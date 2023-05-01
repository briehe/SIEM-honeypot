# SIEM-honeypot
I created a live SIEM with an attack map using Microsoft's Azure platform to create a Windows 10 virtual machine, alongside it's log analytics workspace and Sentinel feature, to create a project for at-home SIEM lab.

![dashboard](https://github.com/briehe/SIEM-honeypot/blob/4242ea8bde250a5e1347a74a8e12dcb7a108b426/failed_rdp_data-dashboard.png)

By opening the virtual machine up to the internet (Disabling the Windows and Azure safety measures, including firewall), I created a \"honeypot\" machine to track the number of failed Remote Desktop Protocol logins attempted on the machine over a three day period. I utilized a script that fed the IP addresses of each failed attempt into an API for geolocation purposes, and this data was fed back into Azure's log analytics workspace to create a live SIEM and attack map inside of Sentinel to measure each attack.

This project was kept alive for three days, after which it was terminated and the resulting data from the virtual machine was harvested for further post-op data analysis.

This repo contains several screenshots from the project while it was live in Azure, as well as the data that was harvested and a small Power BI-generated report from that data.

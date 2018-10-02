How to monitor a VMware vSphere Environment using Telegraf, InfluxDB and Grafana
===================
Once you import the Grafana Dashboards on your Environment, it should look all like these:

*VMware vSphere Overview Dashboard*
![VMware vSphere Overview Dashboard](https://www.jorgedelacruz.es/wp-content/uploads/2018/10/grafana-esxi-022.png)

*VMware vSphere Hosts Dashboard*
![VMware vSphere Hosts Dashboard](https://www.jorgedelacruz.es/wp-content/uploads/2018/10/grafana-esxi-020.png)

*VMware vSphere Datastores Dashboard*
![VMware vSphere Datastores Dashboard](https://www.jorgedelacruz.es/wp-content/uploads/2018/10/grafana-esxi-019.png)

*VMware vSphere VMs Dashboard*
![VMware vSphere VMs Dashboard](https://www.jorgedelacruz.es/wp-content/uploads/2018/10/grafana-esxi-018.png)

----------

### Getting started
You can follow the steps on the next Blog Post in English - https://jorgedelacruz.uk/2018/10/01/looking-for-the-perfect-dashboard-influxdb-telegraf-and-grafana-part-xii-native-telegraf-plugin-for-vsphere/

But in case you want a quick bullet point list:
* Make sure you have Telegraf v1.8.0 or above, then read about the vSphere Plugin here - https://github.com/influxdata/telegraf/tree/release-1.8/plugins/inputs/vsphere
* Edit the vSphere Plugin and add your vCenter IP or FQDN, user and credentials, and enable the sections you want to monitor or exclude from your vSphere.
* Restart the Telegraf service
* Download the VMware vSphere Grafana Dashboards JSON filee and import them into your Grafana
* Enjoy (:

----------

### Additional Information
* This repository it's just intended to provide the Dashboard json files and some help

----------

## Legacy steps for PowerShell Information
This project consists in two Powershell scripts by Mike Nisk - https://github.com/vmkdaily to retrieve the vSphere information and send it directly to InfluxDB, then in Grafana: a Dashboard is created to present all the information.

### Getting started
You can follow the steps on the next Blog Post in Spanish - https://www.jorgedelacruz.es/2017/06/12/en-busca-del-dashboard-perfecto-influxdb-telegraf-y-grafana-parte-vii-monitorizar-vsphere/

But in case you can't read Spanish:
* Download the Scripts from the official repo https://github.com/vmkdaily/vFlux-Stats-Kit to the computer you want to run the Scripts periodically
* You should have VMware PowerCLI on this machine
* Edit the Scripts and add your InfluxDB IP or FQDN, InfluxDB users and Database, logging, etc.
* Run the Scripts to check that you can retrieve the information properly
* Schedule the Scripts in Windows to run every X minutes, where you decide the X
* Download the VMware Stats Grafana JSON file and import it into your Grafana
* Change your inforamtion inside the Grafana and enjoy :)

VMware vSphere Overview Dashboard using PowerShell
![alt tag](https://www.jorgedelacruz.es/wp-content/uploads/2017/06/grafana-esxi-013-2.png)

## Legacy steps for PowerShell Information (Not recommended anymore)
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

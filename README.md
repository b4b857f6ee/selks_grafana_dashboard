# Grafana Dashboards for SELKS

You already have :
- Grafana 7+  https://grafana.com/
- SELKS  https://www.stamus-networks.com/scirius-open-source

Preparation : 
- Configure The elasticsearch from SELKS to expose the 9200
- And that's it :)

Configuration 

In the Grafana configuration  -> Data Sources -> "Add data source" -> Select in the section "Logging & document databases" Elasticsearch.
Configure the URL http://SELKSIP:9200/
Access : Server (default)
Index name :  logstash-*  (Pattern No pattern)
Time Field name : @timestamp
Version : 7.0+

-> Save & Test

Help : If it's not working test a curl on your grafana host in destination of SELKS  : curl -X GET "http://SELKSIP:9200/_cluster/health?pretty=true"

And after import the Dashboard in the SELKS folder of this github :)

## NOC configuration

Configure telegraf with influxDB and this script : https://github.com/ratibor78/srvstatus

Configuration of /opt/srvstatus/settings.ini

[SERVICES]
name = ssh.service rsyslog.service  suricata.service elasticsearch.service logstash.service kibana.service evebox.service molochviewer-selks.service molochpcapread-selks.service

## NOC - Services

Grafana Hosted : - https://grafana.com/grafana/dashboards/13235

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/NOC%20-%20Services%20-1.PNG)

# Releases notes

v0.3 Update Dashboard
- NOC - Services -> Add service visualisation and services over time.

v0.2 Add Dashboard
- KRB5
- NFS
- DNP3
- NOC - Services

v0.1 First release


# Todo :
- Add dashboard for :
- RFB
- Improve hunting options
- Add Dashboard for service supervision (NOC)


## Grafana hosted
- SN-ALERTS https://grafana.com/grafana/dashboards/13204
- SN-ALL https://grafana.com/grafana/dashboards/13205
- SN-ANOMALY https://grafana.com/grafana/dashboards/13206
- SN-DHCP https://grafana.com/grafana/dashboards/13207
- SN-DNP3 https://grafana.com/grafana/dashboards/13232
- SN-DNS https://grafana.com/grafana/dashboards/13208
- SN-FILE-Transactions https://grafana.com/grafana/dashboards/13209
- SN-FLOW https://grafana.com/grafana/dashboards/13210
- SN-HTTP https://grafana.com/grafana/dashboards/13211
- SN-IDS https://grafana.com/grafana/dashboards/13212
- SN-IKEv2 https://grafana.com/grafana/dashboards/13213
- SN-KRB5 https://grafana.com/grafana/dashboards/13233
- SN-NFS https://grafana.com/grafana/dashboards/13234
- SN-OVERVIEW https://grafana.com/grafana/dashboards/13214
- SN-RDP https://grafana.com/grafana/dashboards/13215
- SN-SIP https://grafana.com/grafana/dashboards/13216
- SN-SMB https://grafana.com/grafana/dashboards/13217
- SN-SNMP https://grafana.com/grafana/dashboards/13218
- SN-SSH https://grafana.com/grafana/dashboards/13219
- SN-STATS https://grafana.com/grafana/dashboards/13220
- SN-FLOW https://grafana.com/grafana/dashboards/13210
- SN-TFTP https://grafana.com/grafana/dashboards/13224
- SN-TLS https://grafana.com/grafana/dashboards/13225
- SN-TrafficID https://grafana.com/grafana/dashboards/13226
- SN-VLAN https://grafana.com/grafana/dashboards/13227

## SN-ALERTS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ALERTS.PNG)

## SN-ALL

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ALL.PNG)

## SN-ANOMALY

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ANOMALY.PNG)

## SN-DHCP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-DHCP.PNG)

## SN-DNP3

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-DNP3.PNG)

## SN-DNS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-DNS.PNG)

## SN-FILE-Transactions

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-FILE-Transactions.PNG)

## SN-FLOW

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-FLOW.PNG)

## SN-HTTP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-HTTP.PNG)

## SN-IDS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-IDS.PNG)

## SN-IKEv2

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-IKEv2.PNG)

## SN-KRB5

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-KRB5-1.PNG)

## SN-NFS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-NFS-1.PNG)

## SN-OVERVIEW

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-OVERVIEW.PNG)

## SN-RDP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-RDP.PNG)

## SN-SIP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-SIP.PNG)

## SN-SMB

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-SMB.PNG)

## SN-SNMP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-SNMP.PNG)

## SN-SSH

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-SSH.PNG)

## SN-STATS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-STATS.PNG)

## SN-TFTP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-TFTP.PNG)

## SN-TLS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-TLS.PNG)

## SN-TrafficID

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-TrafficID.PNG)

## SN-VLAN

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-VLAN.PNG)


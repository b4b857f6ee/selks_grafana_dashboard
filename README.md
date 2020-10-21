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

# Releases notes
v0.1 First release


# Todo :
- Add dashboard for :
- KRB5
- NFS
- RFB
- Improve hunting options
- Add Dashboard for service supervision (NOC)




## SN-ALERTS

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ALERTS.PNG)

## SN-ALL

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ALL.PNG)

## SN-ANOMALY

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-ANOMALY.PNG)

## SN-DHCP

![alt text](https://github.com/b4b857f6ee/selks_grafana_dashboard/blob/main/pictures/SN-DHCP.PNG)

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


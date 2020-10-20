# Dashboard SELKS for Grafana

You already have :
- Grafana 7+  https://grafana.com/
- SELKS  https://www.stamus-networks.com/scirius-open-source

Preparation : 
- Configure The elasticsearch from SELKS to expose the 9200
- And that's it :)

Configuration 

On Grafana Configuration  -> Data Sources -> "Add data source" -> Select in the section "Logging & document databases" Elasticsearch.
Configure the URL http://SELKSIP:9200/
Access : Server (default)
Index name :  logstash-*  (Pattern No pattern)
Time Field name : @timestamp
Version : 7.0+

-> Save & Test

Help : If it's not working test a curl on your grafana host in destination of SELKS  : curl -X GET "http://SELKSIP:9200/_cluster/health?pretty=true"

And after import the Dashboard in the SELKS folder of this github :)

Releases notes
________________________________
v0.1 First release


Todo :
Add dashboard for :
KRB5
NFS
RFB
Improve hunting options

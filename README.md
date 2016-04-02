# Grafana Zenoss Annotations plugin

**Plugin will be available soon for Grafana 3.0.**

The Zenoss plugin is very flexible Grafana 3.0 plugin, which allow Grafana to
display annotations/events from your Zenoss instance.

![Grafana Zenoss plugin](https://raw.githubusercontent.com/monitoringartist/grafana-zenoss-annotations/master/doc/grafana-zenoss-plugin.gif)

Supported Zenoss versions:

- Zenoss Core 5.x
- Zenoss Resource Manager 5.x
- Zenoss Core 4.2.x
- Zenoss Resource Manager 4.2.x

It's paid plugin a is distributed only as a private Docker image.

# Installation

```
# initialize Grafana Zenoss Annotations plugin container (private Docker image)
docker run \
  -d \
  --name zenoss-annotations \
  monitoringartist/zenoss-annotations:latest

# create /var/lib/grafana as persistent volume storage
docker run \
  -d \
  --name grafana-xxl-storage \
  -v /var/lib/grafana \
   busybox:latest

# start grafana-xxl
docker run \
  -d \
  -p 3000:3000 \
  --name grafana-xxl \
  --volumes-from grafana-xxl-storage \
  --volumes-from zenoss-annotations \
  monitoringartist/grafana-xxl:3.0
```

# Grafana support

We are happy to help you with any your Grafana issues. Please contact us
info@monitoringartist.com and ask for our professional consulting services.

# Author

[Devops Monitoring zExpert](http://www.jangaraj.com 'DevOps / Docker / Kubernetes / Zabbix / Zenoss / Monitoring'),
who loves monitoring systems, which start with letter Z. Those are Zabbix and Zenoss.

Professional monitoring services:

[![Monitoring Artist](http://monitoringartist.com/img/github-monitoring-artist-logo.jpg)](http://www.monitoringartist.com 'DevOps / Docker / Kubernetes / Zabbix / Zenoss / Monitoring')

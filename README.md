## Welcome to EidenWorks

This is a project intended to aggregate different sources of information from Cloud Deployments (OpenStack, Kubernetes, Containers, Operating System ...) using tools from the Big Data ecosystem.

### Why?

The origin of this project comes from a prototype done by Red Hat's Strategic Design Team and [KEEDIO](http://keedio.com) to investigate the different ways to perform log aggregation. 

The initial target of the prototype is to aggregate logs from an OpenStack deployment for the OpenStack Operator Persona, howevernt he following data types are considered to be aggregated:
- Logs
- Metrics
- Events 
- Configuration

To understand the concept you may go throught there blog posts:
- [Ops Happiness: The Quest for Operations Intelligence](http://rhelblog.redhat.com/2017/02/06/ops-happiness-the-quest-for-operations-intelligence/)
- [Ops Happiness – Harness Data for Operations Intelligence](http://rhelblog.redhat.com/2017/02/15/ops-happiness-harness-data-for-operations-intelligence/)
- [Events and Monitoring Supercharging your Operational Intelligence](http://rhelblog.redhat.com/2017/03/30/events-and-monitoring-supercharging-your-operational-intelligence/)

### Status

There is a running prototype set up on a test lab with half the services manually deployed in VMs on OpenStack and the other half on Containers on OpenShift.

The toolchain selected is the following
```
rsyslog --> nifi --> kafka --> flink --> cassandra --> patternfly
```

All the content is available in the [main](https://github.com/eidenworks) repository.

All the configuration files used in the prototype are uploaded to the [configfiles](https://github.com/eidenworks/configfiles) repository.

There is initial work being done to package all components. You may want to check [Eidenworks COPR repo](https://copr.fedorainfracloud.org/coprs/mperezco/eidenworks/)


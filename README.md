GeoPaaS Lite on OSE3
=================
This builds on the http://geopaas.io demo by Jason Callaway.  On your OpenShift 3 development box you'll want to clone this repository.

Clone the docker-geosuite repository
```
git clone https://github.com/openshift-geopaas/openshift-geopaas.git
```
Create a project for this deployment
```
oc new-project geopaas
```
Create the GeoSuite template
```
oc create -f geopaas-lite-template.yaml
```
Navigate to your master
```
https://master.ose3.exmaple.com:8443
```
Click on "Add to Project"

Click on "Show All Templates"

Find "GeoPaaS Lite" and click it

Accept the defaults and click "Create"

The builds won't start automatically.  On the left click "Browse" then "Builds".

For the "geoexplorer" and "geoserver" click "Start Build".  These can be run simultaneously.

When the build completes, the deployments WILL start automatically.  When they are done, you can navigate to each page.

Note
---
The BuildConfigs in the template use the "DockerStrategy" for builds.

# MapIt

MapIt is a geo-spatial Spring Boot app which shows the location of AirPorts on the Map using Leaflet. This app is a
port of a [python app](https://github.com/thesteve0/awsdemo) originally created by [Steven Pousty](https://github.com/thesteve0).

# Deploy Guide

You can deploy MapIt on OpenShift using the provided template:
```
oc new-project mapit
oc new-app https://github.com/stepgrif/mapit-spring.git --strategy=pipeline
oc import-image my-redhat-openjdk-18/openjdk18-openshift --from=registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift --confirm
...
...
oc new-app -f https://raw.githubusercontent.com/siamaksade/mapit-spring/master/mapit-template.yaml
```


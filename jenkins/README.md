# Jenkins

```
oc new-project jenkins
oc new-project petclinic-dev
oc new-project petclinic-prod

oc new-app jenkins


oc policy add-role-to-group edit system:serviceaccounts:jenkins -n petclinic-dev
oc policy add-role-to-group edit system:serviceaccounts:jenkins -n petclinic-prod

oc create -f pipeline.yaml

oc start-build petclinic-pipeline
``` 

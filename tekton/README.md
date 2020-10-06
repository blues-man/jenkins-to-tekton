# Tekton

```
oc new-project tekton

oc new-project petclinic-dev
oc new-project petclinic-prod

oc policy add-role-to-group edit system:serviceaccounts:tekton -n petclinic-dev
oc policy add-role-to-group edit system:serviceaccounts:tekton -n petclinic-prod

oc create secret generic git-secret --from-literal=username=<USER> --from-literal=password=<PASS>
oc annotate secret git-secret "tekton.dev/git-0=https://gitea-gitea.apps.cluster-wkrhtr.red.osp.opentlc.com"
oc secrets link pipeline git-secret

oc create -f pvc
oc create -f tasks
oc create -f pipelines
oc create -f pipelineruns
```


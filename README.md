# Helm Intro

Use this chart to demo Helm on OpenShift! This is based on the default chart
created with `helm create <chart>`.

## How to Use

1. Create a new project: `$ oc new-project helm-intro`
2. Allow default Nginx container to run in OpenShift: `$ oc adm policy add-scc-to-user anyuid -z default`
3. Deploy the chart with Helm: `$ helm install helm-intro .`
4. Expose the service created by the chart: `$ oc expose svc/helm-intro`
5. Get the URL of the new route: `$ oc get routes/helm-intro`
6. Navigate to the URL in a browser to test
7. Change `myApp.greeting` in *values.yaml* to something else
8. Update application running on OpenShift using Helm: `$ helm upgrade helm-intro .`

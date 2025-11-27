# DO180 – OpenShift Route Practical  
> **This repository is a demo of OpenShift S2I (Source-to-Image)**, demonstrating how to build and run applications directly from a Git repository using `oc new-app`.

This repository contains the source code (`index.php`) and the steps used to deploy the application on OpenShift using S2I, expose the service, and verify the route.
## 🚀 Deploy Application on OpenShift

### 
1️⃣ Create application from Git repo
oc new-app https://github.com/Openshift-Imp/do180.git

2️⃣ Check build logs
oc logs bc/do180

3️⃣ Verify pods
oc get pods

4️⃣ Check deployment
oc get deployment

5️⃣ Check service
oc get svc

6️⃣ Test application using ClusterIP
curl <cluster-ip>:8080
# Example:
curl 172.30.226.199:8080

7️⃣ Expose route
oc expose svc do180

8️⃣ Check route
oc get route

🌐 Access Application

After exposing the service, access the URL shown under:

oc get route
Example:
do180-dhiraj7744-dev.apps.rm2.thpm.p1.openshiftapps.com

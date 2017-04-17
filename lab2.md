# 2. Performing a build and deployment of an application (oc client)

1. Perform the following sequence of commands:

```
oc login https://10.1.2.2:8443 -u openshift-dev

# Enter your password if prompted

oc --help

oc version

oc status

oc get all

# Let's deploy the php app from your specific branch
oc new-app php~<php app repo>#<your branch name> --name=<name of your app>

oc get all

# Let's create a route
oc get svc

oc expose svc <name of your app service>

oc get bc

oc get bc <bc name> -o yaml
```
Now make a code change in your branch, commit, and push it in. Then:

```
oc start-build <name of your app>
```

_But what if we want to make rapid changes without having to trigger a re-build and re-deploy every time?_

```
cd <root directory of your local copy of your repo branch>

# get the pod name
oc get pods

oc rsync . <pod name>:/opt/app-root/src --watch

```

In Eclipse, make changes to the `image.php` file like commenting out the blue box and uncommenting the green box. Once done, save the file. You'll note in your terminal session that the rsync has sent the changes to the pod.

Now refresh your browser window and you'll see the change.

Continue in this fashion and make any changes you would like, and simply refresh the browser as you would normally to see the changes reflected as you continue to code.

[Back to Main Page](index.md)

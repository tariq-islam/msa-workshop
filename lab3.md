# Deploying The Microservices Application
### The power of templates

Before we begin, please import the microservices repo _(your specific branch!)_ locally into Eclipse.

There are a lot of directories but what we are going to concern ourselves with is the `./labs/lab3` and `./labs/lab3_ocp` directories.

## The Template
Looking at your repo branch, you should have a template. Let's open that up (`foodwine-template.json`) and explore it.

There are a couple of ways to deploy this:
#### CLI:
```
oc process -f labs/lab3_ocp/templates/foodwineapp-template.json | oc create -f -
```

#### Eclipse:
1. Right click on your project
2. Select `New >> Resource`
3. In the window that pops up, select `Browse Workspace`.
4. Navigate to `labs/lab3_ocp/templates/foodwineapp-template.json` and select it.
5. Click `Finish`
![Image](3_1.png)

6. Back in the OpenShift Explorer view, right click on your project and select `New >> Application`
7. In the pop up window, scroll down until you find the `wineapp` template that you just imported. Click `Next`.
8. In the next window, select the `APPLICATION_DOMAIN` value and edit it. Change it to your OpenShift subdomain. For the CDK this is `10.1.2.2.nip.io`.
![Image](3_2.png)

9. Click `Finish`

10. Click `Ok` in the resource creation confirmation window.

11. Click `Cancel` on the repo import pop up window as you have already imported your repo branch into Eclipse.


[Back to Main Page](index.md)

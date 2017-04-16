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




[Back to Main Page](index.md)

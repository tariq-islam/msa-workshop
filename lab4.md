# Let's Get Creative.

In this lab you'll have the freedom to make whatever changes you wish through whichever mechanism you desire as we have covered today (Web UI, Eclipse, oc client).

Feel free to

If you break your deployment in any way, simply run the following command and re-process the template:
```
oc delete all --all --now

# Then from your local repo

oc process -f labs/lab3_ocp/templates/foodwineapp-template.json | oc create -f -
```

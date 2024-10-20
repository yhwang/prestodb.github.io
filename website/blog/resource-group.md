Presto Console - Resource Group

If you are setting up a Presto Cluster for multiple groups or users, the `Resource Group` feature
allows you to arrange the CPU time, memory usage, and number of running queries for each group.
Check the [documentation](https://prestodb.io/docs/current/admin/resource-groups.html)
for more details. To query the resource group statistics after the feature has been turned on,
you can access the REST API on the coordinator using the `/v1/resourceGroupState/` endpoint
to retrieve the resource group information. More easily, you can access the resource groups
information by accessing the `RESOURCE GROUPS` page on the Presto Console. On the top banner
of the Presto Console, you can find the `RESOURCE GROUPS` page:
![resource-group-tab](./images/resource-group-page.png)
The link leads you to the `root` resource group and shows its statistics. Or you can click
on the

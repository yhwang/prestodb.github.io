Presto Console - Resource Group

If you set up a Presto Cluster for multiple groups or users, you may configure the corresponding
`Resource Group` settings to arrange the CPU time, memory usage, and number of running queries
for different groups. If not, check the [documentation](https://prestodb.io/docs/current/admin/resource-groups.html)
for the details. To query the resource group statistics after the feature has been turned on,
you can access the REST API on the coordinator using the `/v1/resourceGroupState/` endpoint
to retrieve the resource group statistics. Another easier approach is to use the `RESOURCE GROUPS` page
on the Presto Console. On the top banner of the Presto Console, you can find the `RESOURCE GROUPS` page:
![resource-group-tab](./images/resource-group-page.png)

The link leads you to the `root` resource group and shows its statistics. Or you can click
on the resource group link of a query in the `Query Details` section on the `CLUSTER OVERVIEW` page:
![query-details](./images/query-details.png)

The links in the “Query Details” section provide a hierarchical view of the resource group. You can click
on either the root node or a leaf node of the resource group that the query belongs to. For instance,
the query in the screenshot above is associated with the “console” subgroup, which falls under the “adhoc” subgroup.
The “adhoc” subgroup is a part of the “global” resource group. By clicking on each individual node,
you can access the statistics for the respective subgroup. Here’s an example of a subgroup’s statistics:
![show-resource-group](./images/show-resource-group.png)

You can use the `Resource Group` links at the top to navigate to the parent group. In the `Information`
section, you can check the real-time statistics, including `State`, `Schedule Policy`, `Schedule Weight`,
`Soft Memory Limit`, `Soft Concurrency Limit`, `Hard Concurrency Limit`, `Max Queued Queries`,
`Eligible SubGroups`, `Query Limit`, and `Sub-Groups`. [Here](https://prestodb.io/docs/current/admin/resource-groups.html#resource-group-properties)
are the details of each item. The `Timeline` section presents the historical statistics within 5 minutes.
At the very bottom, it lists current running queries if any.

The `Resource Groups` page offers a more convenient way to monitor and verify the resource utilization across
various resource groups on the cluster. You can easily determine the number of resources being used or the
number of queuing queries in a specific resource group. Based on this information, you can make necessary
adjustments to the resource group configuration to prevent resource exhaustion while ensuring that sufficient
resources are allocated for critical users or groups.

Be sure to check out the [documentation](https://prestodb.io/docs/current/admin/resource-groups.html) of the resource group,
set up file-based or database-based resource management, and use the `RESOURCE GROUPS` page to monitor the resource usage.

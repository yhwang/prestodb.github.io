Presto Console - Resource Group

If you are setting up a Presto Cluster for multiple groups or users, the `Resource Group` feature
provides a great way to control the CPU time, memory usage, and number of running queries based on the limitations
you configure for each group. Check the [documentation](https://prestodb.io/docs/current/admin/resource-groups.html)
for more details. To query the resource group statistics, you can access the REST API on the coordinator using the
`/v1/resourceGroupState/` endpoint to retrieve the resource group information.

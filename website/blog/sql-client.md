Presto Console - SQL Client on Web UI


The Presto command line interface (CLI) is one of the de facto tools for interacting with the Presto SQL engine.
To use it, you need to download the jar file and a Java runtime. You can find detailed information
[here](https://prestodb.io/docs/current/installation/cli.html). Thanks to the [Bhuma](https://www.bhuma.dev/) team
for contributing the [presto-js-client](https://github.com/prestodb/presto-js-client) to the Presto community.
The presto-js-client enables the capability to communicate with the Presto SQL engine using JavaScript, one of the
trending programming languages. To extend the benefits of the presto-js-client even further, the Presto Console was
added to the Presto UI in version 0.286. Now you can issue the SQL queries directly from the browsers. Let's walk
through the features that the Presto Console provides.

First thing first, open the Presto web UI on a browser and click on the `SQL Client` at the top banner to view the
UX of the Presto Console:
![sql-client](https://github.com/user-attachments/assets/064d467a-5007-4f3e-8b50-9963064bece9)

The UX of the Presto Console is quite simple and self-explanatory. There is a dismissible message box mentioning
how to set up the access controls and authorization policies to manage accessibility to the Presto Console. You can
close it by clicking the cross sign on the upper right corner of the message box. The main UX is comprised of two
dropdown lists, `Catalog` and `Schema`, a `Run` button, and a SQL input text area.
![sql-client](https://github.com/user-attachments/assets/abec250a-ccb3-49aa-b31c-02d7cb5d38c8)

Use the `Catalog` and `Schema` drop-down lists to select the default catalog and schema for the SQL query. When you
select a catalog, the `Schema` drop-down list will show you the available schemas. Once the catalog and schema are
specified, they become the default values for the SQL query. To conserve the memory footprint used by the Presto
Console, a `SELECT` query will be limited to 100 returned records by appending `limit 100` to the end when you click
the `Run` button. The query results are presented in a table view below the SQL input. Here is an example of running a
[TPCH query](https://github.com/prestodb/presto/blob/master/presto-benchto-benchmarks/src/main/resources/sql/presto/tpch/q18.sql):
![query-example](https://github.com/user-attachments/assets/f1529040-caec-4927-87cb-d64b008e4154)

Use the navigation bar at the bottom of the table to view the results. If you are interested in the query plan for the SQL query,
you can click the link at the top of the table to get detailed information.

In version 0.287, session properties support is added to the Presto Console. You can modify the session properties in the
`Session Properties` tab and switch back to the `SQL` tab to type in and run the SQL query. Be sure the hit the `Enter` key after
you type the new value for a session property. The session properties you changed are highlighted in a different color, like this:
![session-property](https://github.com/user-attachments/assets/5c39db3c-1d58-455f-aa7a-6fd329b67c09)

That's all about the Presto Console. Hope you like it and find it useful. If you'd like to see any features in
the Presto Console, feel free to open an issue at the [prestodb/presto](https://github.com/prestodb/presto) repository.


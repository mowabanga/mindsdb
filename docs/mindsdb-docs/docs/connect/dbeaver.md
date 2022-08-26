# MindsDB and DBeaver

DBeaver is a database tool that allows you to connect to and work with various database engines. You can download it [here](https://dbeaver.io/).

## Data Setup

First, you create a new database connection in DBeaver by clicking the icon, as shown below.

![New Database Connection](/assets/sql/dbeaver_1.png)

Next, choose the MySQL database engine and click the *Next* button.

![Choose database engine](/assets/sql/dbeaver_2.png)

Now it's the time to fill in the connection details.

![Connection details](/assets/sql/dbeaver_3.png)

There are two options, as below.

=== "Connecting to your MindsDB Cloud account"

    You can connect to your MindsDB Cloud account. To do that, please use the connection details below:<br/>

    &emsp;&emsp;Hostname: `cloud-mysql.mindsdb.com`<br/>
    &emsp;&emsp;Port: `3306`<br/>
    &emsp;&emsp;Username: *your MindsDB Cloud username*<br/>
    &emsp;&emsp;Password: *your MindsDB Cloud password*<br/>
    &emsp;&emsp;Database: *leave it empty*<br/>

=== "Connecting to your local MindsDB"

    You can connect to your local MindsDB. To do that, please use the connection details below:<br/>

    &emsp;&emsp;Hostname: `127.0.0.1`<br/>
    &emsp;&emsp;Port: `47334`<br/>
    &emsp;&emsp;Username: `mindsdb`<br/>
    &emsp;&emsp;Password: *leave it empty*<br/>
    &emsp;&emsp;Database: *leave it empty*<br/>

Now we are ready to test the connection.

## Testing the Connection

Click on the `Test Connection...` button to check if all the provided data allows you to connect to MindsDB

![Connection test](/assets/sql/dbeaver_4.png)

On success, you should see the message, as shown above.

## Let's Run Some Queries

To finally make sure that our MinsdDB database connection works, let's run some queries.

```sql
SELECT *
FROM mindsdb.predictors;
```

On execution, we get:

```sql
+-------------------------+--------+------------------+------------------+-------------+---------------+-----+-----------------+----------------+
|name                     |status  |accuracy          |predict           |update_status|mindsdb_version|error|select_data_query|training_options|
+-------------------------+--------+------------------+------------------+-------------+---------------+-----+-----------------+----------------+
|house_sales_model        |complete|0.4658770134240238|ma                |up_to_date   |22.7.5.1       |     |                 |                |
|process_quality_predictor|complete|1.0               |silica_concentrate|up_to_date   |22.7.5.1       |     |                 |                |
|home_rentals_model       |complete|0.9991920992432087|rental_price      |up_to_date   |22.7.4.0       |     |                 |                |
+-------------------------+--------+------------------+------------------+-------------+---------------+-----+-----------------+----------------+
```

Here is how it looks in DBeaver:

![Query test](/assets/sql/dbeaver_5.png)

!!! tip "Whitelist MindsDB Cloud IP address"
    If you need to whitelist the MindsDB Cloud IP address to gain access to your database, reach out to the MindsDB team, and we'll share the MindsDB Cloud static IP address with you.

## What's Next?

Now that you are all set, we recommend you check out our **Tutorials** and **Community Tutorials** sections, where you'll find various examples of regression, classification, and time series predictions with MindsDB.

To learn more about MindsDB itself, follow the guide on [MindsDB database structure](/sql/table-structure/). Also, don't miss out on the remaining pages from the **SQL API** section, as they explain a common SQL syntax with examples.

Have fun!
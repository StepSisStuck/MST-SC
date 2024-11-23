# Understanding the payload

```sql
' OR 1=1; -- -
```
This code snippet is a classic example of a SQL injection payload. Let's break it down:

- `'` is a single quote character that closes the string.
- `OR 1=1` is a condition that always evaluates to true. This condition is used to bypass the authentication mechanism.
- `;` is a semicolon that terminates the current SQL statement.
- `--` is a comment that ignores the rest of the query.
- `-` is a hyphen that helps to comment out the remaining part of the query.

When this payload is injected into a vulnerable SQL query, it effectively changes the query to `SELECT * FROM users WHERE username = '' OR 1=1; -- -' AND password = 'password'`. This query will return all rows from the `users` table, effectively bypassing the authentication mechanism.

- So this command will return all the rows from the users table, effectively bypassing the authentication mechanism.



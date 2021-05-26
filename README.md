# Bank Web App

## Installation and Setup

#### NPM installs

```
npm install xss-filters
npm install express
npm install client-sessions
npm install mysql2
npm install helmet-csp

```
#### Msqlserver commands

```
CREATE USER 'db1'@'localhost'
IDENTIFIED BY 'Hfd%4g3hf&^FGH'; 
CREATE DATABASE bank;
GRANT SELECT, INSERT, UPDATE, CREATE ON 'bank' TO 'db1'@'localhost';
mysql -u db1 -p bank < bank.sql;
```

## Use cases
```
Register
Log in
Deposit
Withdraw
Transfer
Log out

```

## Security Design Principles
<pre>
<ul>
<li>Input escaping
    XSS-Filters
    Front End Protections pattern requirments<br>
<li>Alphanumeric function
    whitelisting using regular expressions<br>
<li>Input validation
    not nan, not negative, not infinity, not undefined<br>
<li>Content security policy header
    Helmet CSP<br>
<li>Sessions
    Creating a session cookie that lasts 3 min
    User action will reset cookie to 3 min
    Adds broken authentication protections

<li>Injection protection
  Input escaping
  Input validation
  Prepared queries
  Allow-list input validation through regular expressions
  Enforcing least privilege by limiting user db1
  SQL var character limits
</ul>
</pre>

## Authors

* **Alaa Abdin aabdin@csu.fullerton.edu**
* **Paul Smith pgsmith@csu.fullerton.edu** 
* **Benjamin Heng bheng@csu.fullerton.edu**


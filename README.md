# PostgreSql_learning

This Readme file will show the details of my works and my learning output

## What is PostgreSql?
PostgreSql is an open source SQL server for Relational Database system.PostgreSql supports both SQL and JSON(non Realtional) Querying. PostgreSql supports all the common programming languages. PostgreSql has some advanced features that are used for Enterprise and not available in mysql.

>In this Research team, we are using PostgreSql and learning how to use it in cloud and many more.


## Installation

1. ### Install on Linux Mint

    I am using Linux Mint 20 Cinnamon, a debian based Linux Operating System. All the Commands will work on any Debian based Linux distro.

    1. There is a very easy way to install using terminal. copy the following command and your system will autometically install PostgreSql.

    ```bash
    Sudo apt-get update
    ```
    Then enter the following code.

    ```bash
    sudo apt-get install postgresql
    ```
    This will autometically install the latest version that is available for your system from the web.(Internet Connection is required)

    2. You can easily download and follow the instructions from PostgreSql documentation. [click here](https://www.postgresql.org/download/ "Download from here")
   
2. ### Install on Manjaro 21.0.3 Ornara
    Using Terminal, copy-paste the following command
   ```bash
   sudo pacman -S postgresql postgis
   ```
   Terminal will install postgresql libs and postgresql latest verison. Internet connection is required.


## Configuiring the PostgreSql

1. ### Configuration on Linux Mint
    to check that your postgreSql is successfully installed or not, copy the command in terminal and enter.

    ```bash
    service postgresql status
    ```

    If your PostgreSql server is not active, you can active by

    ```bash
    service postgresql start
    ```

    to stop the server, please follow the command,

    ```bash
    service postgresql stop
   ```
2. ### Configuration on Manjaro
    There is a slightly difference between the configuration on Mint and Manjaro. check out the command below

    here postgres is a default username. for password, you should use your system admin password. This command will give access to postgresql bash.
    ```bash
    sudo -iu postgres
    ```

    then, create a cluster by using,
    ```bash
    initdb --locale $LANG -E UTF8 -D '/var/lib/postgres/data/'
    ```
    If there is no error. you are good to go. just exit the bash.
    ```bash
    exit
    ```
    Now, we need to restart our postgresql server. here is the command 
    ```bash
    sudo systemctl enable --now postgresql.service
    ```
    You should get no error. 
    
    To check that your server is working or not, follow the command and hit enter
    ```bash
    sudo systemctl status postgresql
    ```

### How to run PostgreSql in Command line?

You can run PostgreSql using the following command in terminal.

```bash
sudo -u postgres psql
```
or
```bash
psql -U postgres
```

Great! you are now in the PostgreSql sql terminal. Check out the offical documentations for command line. 

to check the Database users, write the command and enter:

```bash
\du
```

List of schemas , type:

```bash
\dn
```

### Create a databse

using command line, you can create a db using:

```sql
CREATE DATABASE dbname;
```

if this replies "CREATE DATABASE" means database has successfully created. there is no error till now.

### show the list of Database

after craeting the database you can check out the list of database in postgresql server.

write the following command in the terminal:

```bash
\l
```

this command will return the list of databases with owners and access privilages.

### Create a database named test

```sql
CREATE DATABASE test;
```

this command will create e new database name test. 

### Check the list again by:
```bash
\l
```


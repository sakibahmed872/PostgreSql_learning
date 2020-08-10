# PostgreSql_learning

This Readme file will show the details of my works and my learning output

## What is PostgreSql?
PostgreSql is an open source SQL server for Relational Database system.PostgreSql supports both SQL and JSON(non Realtional) Querying. PostgreSql supports all the common programming languages. PostgreSql has some advanced features that are used for Enterprise and not available in mysql.

>In this Research team, we are using PostgreSql and learning how to use it in cloud and many more.


## Installation in Linux Mint

I am using Linux Mint 20 Cinnamon, a debian based Linux Operating System.

1. There is a very easy way to install using terminal. copy the following command and your system will autometically install PostgreSql.

    >```Sudo apt-get update ```

    Then enter the following code.

    >```sudo apt-get install postgresql```

    This will autometically install the latest version that is available for your system from the web.(Internet Connection is required)

2. You can easily download and follow the instructions from PostgreSql documentation. [click here](https://www.postgresql.org/download/ "Download from here")


## Configuiring the PostgreSql

to check that your postgreSql is successfully installed or not, copy the command in terminal and enter.

>``` Service postgresql status```

If your PostgreSql server is not active, you can active by

>``` Service postgresql start```

to stop the server, please follow the command,

>```service postgresql stop```

### How to run PostgreSql in Command line?

You can run PostgreSql using the following command in terminal.

>```sudo -u postgres psql```

Great! you are now in the PostgreSql terminal. Check out the offical documentations for command line. 

to check the Database users, write the command and enter:

>```\du```

List of schemas , type:

>```\dn```

### Create a databse

using command line, you can create a db using:

>```creatdb dbname```

if this replies nothing means you are good to go. there is no error till now.

### show the list of Database

after craeting the database you can check out the list of database in postgresql server.

write the following command in the terminal:

>```\l```

this command will return the list of databases with owners and access privilages.
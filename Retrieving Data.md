### Reading data from CSV files
- ##### Import the Data
    - data = pd.read_csv(filepath) 
        - read_csv() function read data from csv files
        - read_csv() returns the data in form of Dataframe

    - iloc()

- ##### Usefull Arguments
    - pd.read_csv(filepath , sep="\t") 
        - [sep] argument tells how the data items are separated in our CSV file
        - by default value is sep = "," '''

    - pd.read_csv(filepath , delim_whitespace = True)
        - [delim_whitespace] specifies that the values are seperated by whitespace
        - anytime there is a whitespace , there is a new value

    - pd.read_csv(filepath , header = None)
        - [header] argument is use to specify which row is to be the header for the column names. 

    - pd.read_csv(filepath , names = ["Name1" , "Name2" ])
        - [names] argument is used to specify the column names.
        - the length of the list of the names should be same as the number of columns.

    - pd.read_csv(filepath , na_values=["NA" , 99])
        - [na_values] argument is used to specify a value or list values which should be considered as NaN(Not a Number) .

### Reading Data from JSON files
- JSON  stands for Java Script Object Notation
- These files are standard way to store data across platforms
- These files have very similar structure to <u>Python dictionaries</u>.
- The Column name is the Key and Value is the value for the column for the specific row. 

- ##### Import Data 
    - data = pd.read_json(filepath)
        - read_json() function read data from JSON files.
        - It returns a dataframe.
    - data.to_json(filename)
        - filename eg. "outputfile.json"
        - to_json() function stores the dataframe into a JSON file.

- ##### Usefull Arguments
    - path/buf:
        - a valid JSON string , path object or file.
        - eg. "file://localhost/path/to/table.json"
    - orient: 
        - Indicate the expected JSON string format.
        - some orient values are ["split" , "records" , "index" , etc.]
    - typ:
        - It specifies the type of the object to be covered 
        - ['frame' , 'series'], default values is 'frame'


### Reading Data from SQL Databases
- Structured Query Language represents a set of relational databases with fixed schemas(predefined structure of tables in the relation databases).
- Examples of SQL Databases.
    - Microsoft SQL Server
    - Postgres 
    - MySQL
    - AWS Redshift
    - Oracle DB
    - Db2 Family 

 - ##### Import Data
    - using Sqlite3 Database
    - for Sqlite3 , library used is [sqlite3]
    - con = sq3.Connection(path) -> Creating connection with the Sqlite Database.
    - data = pd.read_sql(query , con)
        - read_sql() reads the data from the the Sql database
        - It returns the Dataframe from the data.
    - ##### Useful Arguments
        - [query] argument is the SQL command eg. "SELECR * FROM TABLE_NAME"
        - [con] is the connection established with the database
        - [columns] argument is used to the list the column names to select from SQL table (only used when reading a table)

### Reading Data from NoSQL Databases
- Not-only SQL databases are not relational.
- They vary more in structure.
- Most NoSQL databases store data in JSON format.
- Examples of NoSQL Databases:
    - Document Databases: mongoDB , couchDB
        - each document is on observation , like JSON files
    - Key-Value stores : Riak, Redis
        - Key will be like an ID like a person and values will be like their age , address , etc.
    - Graph databases : Neo4j , HyperGraph
        - Use for network anlaysis and maintaining relationships.
    - Wide-column stores : Cassandra , HBase
        - All Columns are collected in a certain column family ,  eg. for a person , personal details might be in one column family and professional in another.

- ##### Import Data
    - using MongoDB
    - for MongoDB , we use [pymongo] library
    - con = MongoClient() -> estanlishing connection with the database
    - con.list_database_names will display the names of the available database.
    - db = con.database_name , this sets the 'db' variable to a specific database here name is 'database_name'
    - to create a cursor object using a 'query'
        - cursor = db.collection_name.find(query)
        - It returns a cursor to the documents that match the selection criteria.
    - df = pd.DataFrame(list(cursor))

### Reading Data from APIs

- ##### Import Data
    - pd.read_csv(dataURL) 





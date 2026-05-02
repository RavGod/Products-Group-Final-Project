# Products-Group-Final-Project

Before running the project, be sure to change the 'spring.datasource.password' value found in the 'demo/src/main/resources/application.properties' file to the password you set up pgAdmin with.

Upon running the project, go to hoppscotch.io. Here, you can access the database using http://localhost:8081/products

Alternatively, you can run the frontend file using the instructions found in the readme of the frontend file.
There, you can access and alter the database using the GUI.

http://localhost:8081/products with the GET method returns a list of every item in the database.

http://localhost:8081/products with the POST method lets you add an item to the database.
Request body format:

 {
    "product_count": 10,
    "product_description": "Example text",
    "product_name": "Example",
    "product_price": 29.99,
    "product_type": "Equipment/Safety/Material",
    "threshold": 5
  }

http://localhost:8081/products/{id} with the PUT method lets you edit an item in the database, also using the same request body format.

http://localhost:8081/products/{id} with the GET method returns a single item from the database if an item with the corresponding ID exists.

http://localhost:8081/products/{id} with the DELETE method deletes the item with the correponding ID if it exists.

The SQL scripts can be found at src/main/resources/db/migration, called 'V1__create_products_table.sql' and 'V2__insert_products.sql'.
To ensure that changes to the script are reflected in the program, be sure to delete the old table before updating it.
These tables are the 'Product' and 'flyway_schema_history' tables.

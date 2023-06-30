**SQL database** 
* **step 1** - dbSetup.sql file
  * create your table
  * **keywords**
  * `CREATE TABLE`, `INSERT`, `FROM`, `WHERE`, `LIKE`, `DELETE`
  * `SELECT`, `AND`, `UPDATE`, `SET`
  * eg' `SELECT` name `FROM` penguins `WHERE` name `LIKE`, "%y%"
  * the above statement says return any penguin where the name has a y
  * `UPDATE` penguins  `SET` ``wearing tuxedo`` = false `WHERE` id = 4
  * 
* **step 2** - dbSetup.sql **reference for inserts**
  * **CREATE TABLE EXAMPLE** 
  *     CREATE TABLE cars(
        id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
        make VARCHAR(100) BOT NULL,
        model VARCHAR(100) BOT NULL,
        year INT NOT NULL DEFAULT 1990,
        price DOUBLE NOT NULL DEFAULT 1.00,
        color VARCHAR(100) NOT NULL,
        description VARCHAR(500),
  
        createdAt DATETIME DEFAULT CURRENT_TIMESTAMP COMMENT 'Time Created',
        updatedAt DATETIME DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
        ) default charset utf8 COMMENT '';

* **Step 3** model -> controller -> repo -> service 
# Learn Bash and SQL by Building a Bike Rental Shop

> Welcome to the Bash and SQL lessons!

## 10. Start the Terminal

### 10.1

**The first thing you need to do is start the terminal.** Do that by clicking the "hamburger" menu at the top left of the screen, going to the
 "terminal" section, and clicking "new terminal". Once you open a new one, type `echo hello terminal` into the terminal and press enter.

#### HINTS

- Capitalization matters
- If the tests don't run automatically, try typing `exit` into the terminal and redoing the instructions

## 20. Log in to Psql

### 20.1

You are going to build a bike rental shop. It will have a database, and a bash script to interact with the database. Use the terminal to conne
ct to PostgreSQL by entering `psql --username=freecodecamp --dbname=postgres`.
#### HINTS

- Type the above command into the terminal and press enter
- Type `psql --username=freecodecamp --dbname=postgres` into the terminal and press enter

## 30. List Databases

### 30.1

List the databases with `\l` to see what databases are here.

#### HINTS

- Type `\l` into the psql prompt and press enter
- Type `psql --username=freecodecamp --dbname=postgres` into the terminal to log in to psql if you aren't logged in first

## 40. Create Database `bikes`

### 40.1

You need your own database for the bike shop. Create a new database named `bikes`.

####- Use the `CREATE DATABASE` keywords
- Here's an example: `CREATE DATABASE database_name;`
- Type `CREATE DATABASE bikes;` into the psql prompt and press enter
- Type `psql --username=freecodecamp --dbname=postgres` into the terminal to log in to psql if you aren't logged in first

## 50. List Databases

### 50.1

List databases again to make sure your database got created.

#### HINTS

- Use the **l**ist shortcut command
- Type `\l` into the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 60. Connect to `bikes`

### 60.1

There it is. **C**onnect to it so you can start building the structure of your bike shop database. 
#### HINTS

- Use the **c**onnect shortcut command
- Add the database name to the command
- It's the `\c` command
- Here's an example: `\c database_name`
- Try entering `\c bikes` into the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 70. Create table `bikes`

### 70.1

Your database needs three tables. One for your bike inventory, one for your customers, and one for the bikes that are rented out. Create a tab
le named `bikes` in your database for the inventory.

#### HINTS

- Use the `CREATE TABLE` keywords
- Don't forget the parenthesis
- Here's an example: `CREATE TABLE table_name();`
- T- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 80. Display the tables

### 80.1

**D**isplay the tables to make sure your table got created.

#### HINTS

- Use the **d**isplay shortcut command
- It's the `\d` command
- Type `\d` into the psql prompt and press enter
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 90. Add column `bike_id`

### 90.1

The table will have a few columns for bike information. First, is a unique ID column. Add a column to the `bikes` table named `bike_id`. Give 
it a type of `SERIAL` and make it a `PRIMARY KEY`.

#### HINTS
- Try entering `CREATE TABLE bikes();` in the psql prompt
 - Use the `ALTER TABLE`, `ADD COLUMN`, `SERIAL`, and `PRIMARY KEY` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE bikes ADD COLUMN bike_id SERIAL PRIMARY KEY;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 100. Display `bikes` Details

### 100.1

Use the **d**isplay command to view the details of the `bikes` table.

#### HINTS

- It's the `\d` command
- Add the table name to the command
- Try entering `\d bikes` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 110. Add `type` column

### 110.1
The first column is set. Add a column named `type` for the type of bike. Make it a `VARCHAR(50)` and give it a constraint of `NOT NULL`.

#### HINTS

- Use the `ALTER TABLE`, `ADD COLUMN`, `VARCHAR(50)`, and `PRIMARY KEY` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE bikes ADD COLUMN type VARCHAR(50) NOT NULL;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 120. Display `bikes` details

### 120.1

Display the details of the `bikes` table again.

#### HINTS

- Use the **d**isplay shortcut command
- Add the table name to the command
- Here's an example: `\d table_name`
- Try entering `\d bikes` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in
- ## 130. Add Column `size`

### 130.1

The first two columns look good. Add a column named `size` to the `bikes` table that is an `INT` and has the `NOT NULL` constraint. This will 
be for the size of each bike.

#### HINTS

- Use the `ALTER TABLE`, `ADD COLUMN`, `INT`, and `NOT NULL` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE bikes ADD COLUMN size INT NOT NULL;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in

## 140. Add Column `available`

### 140.1

Add another column to the table named `available`. Make it a `boolean` and has a constraint of `NOT NULL`. Also give it a default value of `TR
UE`. This will be set to `false` when someone rents out a bike.

#### HINTS
- Use the `ALTER TABLE`, `ADD COLUMN`, `BOOLEAN`, `NOT NULL` and `DEFAULT TRUE` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS DEFAULT;`
- Try entering `ALTER TABLE bikes ADD COLUMN available BOOLEAN NOT NULL DEFAULT TRUE;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in

## 150. Display `bikes` details

### 150.1

Display the details of the `bikes` table again so you can make sure it's how you want it.

#### HINTS

- Use the **d**isplay shortcut command
- Add the table name to the command
- Here's an example: `\d table_name`
- Try entering `\d bikes` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 160. Create Table `customers`

### 160.1
That table is done for now. Create another table named `customers`. It will store a name and phone number for each customer that rents a bike.

#### HINTS

- Use the `CREATE TABLE` keywords
- Don't forget the parenthesis
- Here's an example: `CREATE TABLE table_name();`
- Try entering `CREATE TABLE customers();` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 170. Add Column `customer_id`

### 170.1

Add a `customer_id` column to your new table that is a type of `SERIAL` and make it a `PRIMARY KEY`.

#### HINTS

- Use the `ALTER TABLE`, `ADD COLUMN`, `SERIAL`, and `PRIMARY KEY` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE customers ADD COLUMN customer_id SERIAL PRIMARY KEY;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 180. Display `customers` Details

### 180.1

Display the details of the `customers` table so you can make sure your new column is there.

#### HINTS

- Use the **d**isplay shortcut command
- Add the table name to the command
- Here's an example: `\d table_name`
- Try entering `\d customers` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 190. Add Column `phone`

### 190.1

There it is. Add a column named `phone` for customers phone numbers. Make it a varying character that has a maximum length of `15` characters.
 Also make sure it can't be null, and that it has to be unique.

#### HINTS
- Use the `ALTER TABLE`, `ADD COLUMN`, `VARCHAR()`, `NOT NULL`, and `UNIQUE` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE customers ADD COLUMN phone VARCHAR(15) NOT NULL UNIQUE;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 200. Add Column `name`

### 200.1

Add the last column. Call it `name` and make it a `VARCHAR(40)` that can't be null.

#### HINTS

- Use the `ALTER TABLE`, `ADD COLUMN`, `VARCHAR()`, and `NOT NULL` keywords
- Here's an example: `ALTER TABLE table_name ADD COLUMN column_name TYPE CONSTRAINTS;`
- Try entering `ALTER TABLE customers ADD COLUMN name VARCHAR(40) NOT NULL;` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 210. Display `customers` Details

### 210.1

Display the details of the `customers` table.
#### HINTS

- Use the **d**isplay shortcut command
- Add the table name to the command
- Here's an example: `\d table_name`
- Try entering `\d customers` in the psql prompt
- Type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in first

## 220. Create Table `rentals`







The rent functionality looks like it all works. Delete the `echo Return Menu` line in the `RETURN_MENU` function so you can get started with that.

#### HINTS

- The `RETURN_MENU` function should be empty
- The `RETURN_MENU` function should look like this:
```sh
RETURN_MENU() {

}
```

## 1457. Add comments to RETURN_MENU

### 1457.1

Add three single line comments to the return menu function; `get customer info`, `if not found`, and `send to main menu`, in that order.

#### HINTS

- Here's an example of a single line comment: `# <comment_here>`
- Make sure the comments are in the same order listed
- The comments should be in the `RETURN_MENU` function
- The `RETURN_MENU` function should look like this:
```sh
RETURN_MENU() {
  # get customer info

  # if not found

  # send to main menu

}
```

## 1460. Start the Return Bike Functionality

### 1460.1

Below the `get customer info` comment you just added, print `What's your phone number?` with a new line in front of the sentence.

#### HINTS

- Use `echo` with the `-e` flag and the new line character (`\n`) to print the suggested message
- Use double quotes around the message
- Here's an example: `echo -e "\n<message_here>"`
- Add `echo -e "\nWhat's your phone number?"` below the suggested comment

## 1470. Read PHONE_NUMBER

### 1470.1

Just below that, use `read` to get input into a `PHONE_NUMBER` variable.

#### HINTS

- Here's an example: `read <VARIABLE_NAME>`
- Add `read PHONE_NUMBER` to the suggested area
- Add it below where you print `What's your phone number?`

## 1472. Add CUSTOMER_ID

### 1472.1

Just below that, set the `CUSTOMER_ID` variable to a query that gets the customer ID from the database using the phone number they gave you.

#### HINTS

- Here's an example: `CUSTOMER_ID=$($PSQL "<query_here>")`
- You want to get the `customer_id` column from the customers table using the `PHONE_NUMBER` variable in your condition to get it
- The condition you want is `WHERE phone = '$PHONE_NUMBER'`
- The query looks like this: `SELECT customer_id FROM customers WHERE phone = '$PHONE_NUMBER'`
- Add `CUSTOMER_ID=$($PSQL "SELECT customer_id FROM customers WHERE phone = '$PHONE_NUMBER'")` below the `read PHONE_NUMBER` line in the `RETURN_MENU` function

## 1474. Add if -z CUSTOMER_ID

### 1474.1

If they are in the database, the variable will be their `customer_id`. If not, it will be empty. Below the `if not found` comment, add an `if` statement that checks if it's empty. Put the `send to main menu` comment in the `then` area.

#### HINTS

- Here's an example:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
fi
```
- The condition you want is `-z $CUSTOMER_ID`
- Place the `# send to main menu` comment in the `<STATEMENTS>` area
- The `if` condition should look like this:
```sh
if [[ -z $CUSTOMER_ID ]]
then
  # send to main menu

fi
```

## 1475. Add MAIN_MENU I could not find a record for that phone number

### 1475.1

If the customer isn't found, send them to the main menu with the message `I could not find a record for that phone number.`

#### HINTS

- You want to call the `MAIN_MENU` function with the message as an argument
- Here's an example: `MAIN_MENU "<message_here>"`
- Add `MAIN_MENU "I could not find a record for that phone number."` below the `send to main menu` comment

## 1476. ./bike-shop.sh

### 1476.1

Run the script and go to the return menu. Enter a phone number that is not in the database. When you are done, exit the program.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- Make sure you are in the `project` folder first

## 1478. Add else with comments

### 1478.1

Add an `else` to the `if` condition for if the phone number is found in the database. Place `get customer's rentals`, `if no rentals`, and `send to main menu` in the `else` area as single line comments.

#### HINTS

- Here's an example of a single line comment: `# <comment_here>`
- Make sure the comments are in the same order listed
- The comments should be in the `else` area of the `if [[ -z CUSTOMER_ID ]]` statement
- An `if/else` statement looks like this:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
else
  <STATEMENTS>
fi
```
- The `else` area should look like this:
```sh
else
  # get customer's rentals

  # if no rentals

  # send to main menu

fi
```
- The whole `if` should look like this:
```sh
if [[ -z $CUSTOMER_ID  ]]
then
  # send to main menu
  MAIN_MENU "I could not find a record for that phone number."
else
  # get customer's rentals

  # if no rentals

  # send to main menu

fi
```

## 1480. psql SELECT * FROM bikes

### 1480.1

You want to find out what rentals a customer has using their phone number and display them. You will need to join all the tables. Start by using the psql prompt to view all the data in the `bikes` table.

#### HINTS

- Use the `SELECT` and `FROM` keywords with `*` to view all the data
- Enter `SELECT * FROM bikes;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1485. psql SELECT * FROM bikes LEFT JOIN rentals

### 1485.1

Next, use a `LEFT JOIN` with `bikes` as the left table to join the bikes and rentals tables. Use the `USING` keyword to join the two tables.

#### HINTS

- You need the `SELECT`, `FROM`, `LEFT JOIN`, and `USING` keywords
- Here's an example: `SELECT <column> FROM <table_1> LEFT JOIN <table_2> USING(<foreign_key>)`
- Enter `\d bikes` or `\d rentals` in the psql prompt to view the details of the table and find the foreign key column
- It's the `bike_id` column
- Enter `SELECT * FROM bikes LEFT JOIN rentals USING(bike_id);` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1490. psql SELECT bikes INNER JOIN rentals

### 1490.1

You only need the bikes that are being rented. Use an inner join with the same two tables to only get those. Use the `USING` keyword again.

#### HINTS

- It's an `INNER JOIN`
- You need the `SELECT`, `FROM`, `INNER JOIN`, and `USING` keywords
- Here's an example: `SELECT <column> FROM <table_1> INNER JOIN <table_2> USING(<foreign_key>)`
- Enter `SELECT * FROM bikes INNER JOIN rentals USING(bike_id);` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1500. psql SELECT bikes INNER JOIN rentals INNER JOIN customers

### 1500.1

Add a join to the previous command that joins the last table so you can get the customer information. Use an `INNER JOIN` and the `USING` keyword again.

#### HINTS

- The previous query was `SELECT * FROM bikes INNER JOIN rentals USING(bike_id);`
- Here's an example: `SELECT <column> FROM <table_1> INNER JOIN <table_2> USING(<foreign_key>) INNER JOIN <table_3> USING(foreign_key)`
- Enter `\d rentals` or `\d customers` in the psql prompt to view the details of the table and find the foreign key column
- It's the `customer_id` column
- Enter `SELECT * FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id);` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1510. psql Add conditions to the query

### 1510.1

Add two conditions to the last query to narrow down the results to the bikes that are currently being rented by customer with `555-5555` as their phone number. The second condition should check the `date_returned` column

#### HINTS

- The previous query was `SELECT * FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id);`
- You want to add a `WHERE <condition_1> AND <condition_2>` to the last query
- Use the `IS NULL` keyword to check the `date_returned` in one of the conditions
- The two conditions are `WHERE phone = '555-5555' AND date_returned IS NULL`
- Enter `SELECT * FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1520. psql SELECT only columns

### 1520.1

Now you have all the rentals for one specific customer. Only get the columns you need to display the bike information to them. They are the same three columns you used to display the list of available bikes.

#### HINTS

- The previous query was `SELECT * FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL;`
- The three columns you want are `bike_id`, `type`, and `size`
- Enter `SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1525. psql SELECT ORDER BY

### 1525.1

One more thing, order the results of the last query by their `bike_id` column.

#### HINTS

- The previous query was `SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL;`
- Add `ORDER BY bike_id` to the end of the last query
- Enter `SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL ORDER BY bike_id;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1530. Add CUSTOMER_RENTALS

### 1530.1

That's the query you will need to use to get the bikes a customer is renting. In your script below the `get customer's rentals` comment. Create a `CUSTOMER_RENTALS` variable that gets the rentals for the customer. Use the `PHONE_NUMBER` variable to get them.

#### HINTS

- Here's an example: `CUSTOMER_RENTALS=$($PSQL "<query_here>")`
- You previously entered `SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND date_returned IS NULL ORDER BY bike_id;` in the psql prompt
- All the columns and tables should be in the same order as in the above query
- The query looks like this: `SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '$PHONE_NUMBER' AND date_returned IS NULL ORDER BY bike_id`
- Add `CUSTOMER_RENTALS=$($PSQL "SELECT bike_id, type, size FROM bikes INNER JOIN rentals USING(bike_id) INNER JOIN customers USING(customer_id) WHERE phone = '$PHONE_NUMBER' AND date_returned IS NULL ORDER BY bike_id")` below the `get customer's rentals` comment

## 1540. Add echo CUSTOMER_RENTALS

### 1540.1

Below the variable you just created, use `echo` to print it. Make sure to put double quotes around it.

#### HINTS

- Here's an example: `echo "<variable_here>"`
- Use the variable with `$CUSTOMER_RENTALS`
- Add `echo "$CUSTOMER_RENTALS"` to the suggested area

## 1550. ./bike-shop.sh

### 1550.1

Run the script and go to the return menu. Enter `555-5555` for the phone number to see the rentals for `Me`.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- Make sure you are in the `project` folder first

## 1560. Add if -z CUSTOMER_RENTALS

### 1560.1

The query is working. If the customer has no rentals, the variable will be empty. Below the `if no rentals` comment, add an `if` condition that checks if it's empty. Put the `send to main` menu comment in the `then` area again.

#### HINTS

- Here's an example:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
fi
```
- The condition you want is `-z $CUSTOMER_RENTALS`
- Place the `# send to main menu` comment in the `<STATEMENTS>` area
- The `if` condition should look like this:
```sh
if [[ -z $CUSTOMER_RENTALS ]]
then
  # send to main menu

fi
```

## 1563. Add MAIN_MENU You do not have any bikes rented

### 1563.1

If the customer has no rentals, send them to the main menu with the message `You do not have any bikes rented.` Add the code below the next comment.

#### HINTS

- You want to call the `MAIN_MENU` function with the message as an argument
- Here's an example: `MAIN_MENU "<message_here>"`
- Add `MAIN_MENU "You do not have any bikes rented."` below the `send to main menu` comment

## 1570. Add else with comments

### 1570.1

Add an `else` to the condition for when the customer does have rentals. Place four single line comments in it; `display rented bikes`, `ask for bike to return`, `if not a number`, and `send to main menu`.

#### HINTS

- Here's an example of a single line comment: `# <comment_here>`
- Make sure the comments are in the same order listed
- The comments should be in the `else` area of the `if [[ -z CUSTOMER_RENTALS ]]` statement
- The `else` area should look like this:
```sh
else
  # display rented bikes

  # ask for bike to return

  # if not a number

  # send to main menu

fi
```
- The whole `if` should look like this:
```sh
if [[ -z $CUSTOMER_RENTALS  ]]
then
  # send to main menu
  MAIN_MENU "You do not have any bikes rented."
else
  # display rented bikes

  # ask for bike to return

  # if not a number

  # send to main menu

fi
```

## 1572. Add echo Here are your rentals

### 1572.1

Below the `display rented bikes` comment, print `Here are your rentals:` with a new line in front of it.

#### HINTS

- Use `echo` with the `-e` flag and the new line character (`\n`) to print the suggested message
- Use double quotes around the message
- Here's an example: `echo -e "\n<message_here>"`
- Add `echo -e "\nHere are your rentals:"` below the suggested comment

## 1575. Add echo CUSTOMER_RENTALS

### 1575.1

Move the `echo $CUSTOMER_RENTALS` line to below the line you just printed.

#### HINTS

- Move the suggested code below where you print `Here are your rentals:`
- You should only print the variable in that one spot
- Place the `echo "$CUSTOMER_RENTALS"` line in the suggested spot

## 1578. ./bike-shop.sh

### 1578.1

Run the script and go to the return menu. Enter `555-5555` for the phone number to see the rented bikes.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- Make sure you are in the `project` folder first

## 1580. Add pipe and while loop

### 1580.1

Where you print the list of rented bikes, pipe the command into a `while` loop that reads the data. You should read the data into `BIKE_ID`, `BAR`, `TYPE`, `BAR`, and `SIZE` variables. Make it print each rented bike in the same fashion as the list of available bikes.

#### HINTS

- Here's an example:
```sh
echo "$CUSTOMER_RENTALS" | while read <VARIABLES>
do
  echo <RENTED_BIKE_INFORMATION>
done
```
- The first line should look like this: `echo "$CUSTOMER_RENTALS" | while read BIKE_ID BAR TYPE BAR SIZE`
- The loop should print `1) 27" Mountain Bike` for each bike with the appropriate bike info
- The whole thing looks like this:
```sh
echo "$CUSTOMER_RENTALS" | while read BIKE_ID BAR TYPE BAR SIZE
do
  echo "$BIKE_ID) $SIZE\" $TYPE Bike"
done
```

## 1585. ./bike-shop.sh

### 1585.1

Run the script and go to the return menu. Enter the same phone number again to make sure the list is showing up correctly.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- Make sure you are in the `project` folder first

## 1590. Add echo Which bike would you like to return?

### 1590.1

Below the `ask for bike to return` comment, print `Which one would you like to return?` with a new line in front of it.

#### HINTS

- Use `echo` with the `-e` flag and the new line character (`\n`) to print the suggested message
- Use double quotes around the message
- Here's an example: `echo -e "\n<message_here>"`
- Add `echo -e "\nWhich one would you like to return?"` below the suggested comment

## 1600. read BIKE_ID_TO_RETURN

### 1600.1

Below the line you just printed, read input into a `BIKE_ID_TO_RETURN` variable.

#### HINTS

- Here's an example: `read <VARIABLE_NAME>`
- Add `read BIKE_ID_TO_RETURN` to the suggested area
- Add it below where you print `Which one would you like to return?`

## 1602. Add if BIKE_ID_TO_RETURN not a number

### 1602.1

Below the `if not a number` comment, check if the input for the bike ID to return is a number using the same method you did earlier. Place the `send to main menu` comment in the statement.

#### HINTS

- Here's an example:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
fi
```
- The condition should check that the `$BIKE_ID_TO_RETURN` variable is not a number using the pattern matching operator (`=~`) and the pattern `^[0-9]+$`
- The condition you want is `[[ ! $BIKE_ID_TO_RETURN =~ ^[0-9]+$ ]]`
- Place the `# send to main menu` comment in the `<STATEMENTS>` area
- The `if` condition should look like this:
```sh
if [[ ! $BIKE_ID_TO_RETURN =~ ^[0-9]+$ ]]
then
  # send to main menu

fi
```

## 1605. Add MAIN_MENU That is not a valid bike number

### 1605.1

If they don't input a number, send them to the main menu with `That is not a valid bike number.` as the message.

#### HINTS

- You want to call the `MAIN_MENU` function with the message as an argument
- Here's an example: `MAIN_MENU "<message_here>"`
- Add `MAIN_MENU "That is not a valid bike number."` below the `send to main menu` comment

## 1607. Add else with comments

### 1607.1

Add an `else` for when they do input a number. Place `check if input is rented`, `if input not rented`, and `send to main menu` single line comments in it.

#### HINTS

- Here's an example of a single line comment: `# <comment_here>`
- Make sure the comments are in the same order listed
- The comments should be in the `else` area of the `if [[ ! $BIKE_ID_TO_RETURN =~ ^[0-9]+$ ]]` statement
- The `else` area should look like this:
```sh
else
  # check if input is rented

  # if input not rented

  # send to main menu

fi
```
- The whole `if` should look like this:
```sh
if [[ ! $BIKE_ID_TO_RETURN =~ ^[0-9]+$ ]]
then
  # send to main menu
  MAIN_MENU "That is not a valid bike number."
else
  # check if input is rented

  # if input not rented

  # send to main menu

fi
```

## 1610. psql SELECT rentals INNER JOIN customers

### 1610.1

You need to check if the input is a `bike_id` rented by the customer so you can return it. In the psql prompt, join the `rentals` and `customers` tables with an `INNER JOIN` using the `USING` keyword.

#### HINTS

- You need the `SELECT`, `FROM`, `INNER JOIN`, and `USING` keywords
- Here's an example: `SELECT <column> FROM <table_1> INNER JOIN <table_2> USING(<foreign_key>)`
- Enter `\d rentals` or `\d customers` in the psql prompt to view the details of the table and find the foreign key column
- It's the `customer_id` column
- Enter `SELECT * FROM rentals INNER JOIN customers USING(customer_id);` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1620. psql Add conditions to the query

### 1620.1

Add three conditions to the previous query. Check the `phone`, `bike_id`, and `date_returned` columns to narrow the results to the first bike you rented with `Me`.

#### HINTS

- The previous query was `SELECT * FROM rentals INNER JOIN customers USING(customer_id);`
- You want to add a `WHERE <condition_1> AND <condition_2> AND <condition_3>` to the last query
- Use the `IS NULL` keyword to check the `date_returned` in one of the conditions
- The other two conditions should check the `phone` and `bike_id` of the first rental
- The three conditions are `WHERE phone = '555-5555' AND bike_id = 1 AND date_returned IS NULL`
- Enter `SELECT * FROM rentals INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND bike_id = 1 AND date_returned IS NULL;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1625. psql Only get columns needed

### 1625.1

You only need to know what bike is going to be returned. Narrow the columns from the last query to only get the one column you would need for returning a bike.

#### HINTS

- The previous query was `SELECT * FROM rentals INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND bike_id = 1 AND date_returned IS NULL;`
- Only column you need is the `rental_id` column
- Enter `SELECT rental_id FROM rentals INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND bike_id = 1 AND date_returned IS NULL;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1630. Add RENTAL_ID

### 1630.1

Back in the script, below the `check if input is rented` comment, create a `RENTAL_ID` variable that gets the rental ID of the bike that was input.

#### HINTS

- The input is the `BIKE_ID_TO_RETURN` variable
- Here's an example: `RENTAL_ID=$($PSQL "<query_here>")`
- You previously entered `SELECT rental_id FROM rentals INNER JOIN customers USING(customer_id) WHERE phone = '555-5555' AND bike_id = 1 AND date_returned IS NULL;` in the psql prompt
- Be sure to use the same columns from the above query for the conditions with the `PHONE_NUMBER` and `BIKE_ID_TO_RETURN` variables
- Add `RENTAL_ID=$($PSQL "SELECT rental_id FROM rentals INNER JOIN customers USING(customer_id) WHERE phone = '$PHONE_NUMBER' AND bike_id = $BIKE_ID_TO_RETURN AND date_returned IS NULL")` below the `check if input is rented` comment

## 1640. Add if -z RENTAL_ID

### 1640.1

Below the `if input not rented` comment, add an `if` that checks if the `RENTAL_ID` variable is empty. Place the `send to main menu` comment in the `then` area.

#### HINTS

- Here's an example:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
fi
```
- The condition you want is `-z $RENTAL_ID`
- Place the `# send to main menu` comment in the `<STATEMENTS>` area
- The `if` condition should look like this:
```sh
if [[ -z $RENTAL_ID ]]
then
  # send to main menu

fi
```

## 1645. Add MAIN_MENU You do not have that bike rented

### 1645.1

If the input isn't rented by the given customer, send them to the main menu with `You do not have that bike rented.` as the message.

#### HINTS

- You want to call the `MAIN_MENU` function with the message as an argument
- Here's an example: `MAIN_MENU "<message_here>"`
- Add `MAIN_MENU "You do not have that bike rented."` below the `send to main menu` comment

## 1648. Add else echo Rental ID RENTAL_ID found

### 1648.1

Add an `else` to the `if` condition you just added. Use `echo` to print `Rental ID $RENTAL_ID found` in it so you can see if it's all working.

#### HINTS

- Here's an example:
```sh
if [[ <CONDITION> ]]
then
  <STATEMENTS>
else
  <STATEMENTS>
fi
```
- Place `echo "Rental ID $RENTAL_ID found"` in the else area
- The `if` condition should look like this:
```sh
if [[ -z $RENTAL_ID ]]
then
  # send to main menu
  MAIN_MENU "You do not have that bike rented."
else
  echo "Rental ID $RENTAL_ID found"
fi
```

## 1650. Run the script

### 1650.1

Run the script and go to the return menu. Enter `555-5555` to see the rented bikes. Input a bike that isn't on the list, then go to the menu again and input a bike that is on the list.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- Make sure you are in the `project` folder first

## 1660. Delete echo Rental ID RENTAL_ID found

### 1660.1

Looks like it works. Delete the line where you print the rental ID.

#### HINTS

- Delete the `echo "Rental ID $RENTAL_ID found"` line

## 1680. Add else with comments

### 1680.1

Add three single line comments in the `else` area; `update date_returned`, `set bike availability to true`, and `send to main menu`.

#### HINTS

- Here's an example of a single line comment: `# <comment_here>`
- Make sure the comments are in the same order listed
- The comments should be in the `else` area of the `if [[ -z $RENTAL_ID ]]` statement
- The `else` area should look like this:
```sh
else
  # update date_returned

  # set bike availability to true

  # send to main menu

fi
```
- The whole `if` should look like this:
```sh
if [[ -z $RENTAL_ID ]]
then
  # send to main menu
  MAIN_MENU "You do not have that bike rented."
else
  # update date_returned

  # set bike availability to true

  # send to main menu

fi
```

## 1690. Add RETURN_BIKE_RESULT

### 1690.1

After a person picks a bike to return and you know that it's a bike they have rented, you need to update all the info in the database to return it. Below the `update date_returned` comment, create a `RETURN_BIKE_RESULT` variable that sets the `date_returned` column to `NOW()` for the bike rented. Use the `RENTAL_ID` to figure out which row to update.

#### HINTS

- Here's an example: `RETURN_BIKE_RESULT=$($PSQL "<query_here>")`
- You want to use the `UPDATE`, `SET`, `NOW()`, and `WHERE` keywords in the query
- Here's an example of the query: `UPDATE <table> SET <column> = <value> WHERE <condition>`
- The query you want is `UPDATE rentals SET date_returned = NOW() WHERE rental_id = $RENTAL_ID`
- Add `RETURN_BIKE_RESULT=$($PSQL "UPDATE rentals SET date_returned = NOW() WHERE rental_id = $RENTAL_ID")` below the `update date_returned` comment

## 1710. Add SET_TO_TRUE_RESULT

### 1710.1

That should update the rentals table. Lastly, you need to make the bike available again. Below the `set bike availability to true` comment, create a `SET_TO_TRUE_RESULT` variable that makes the bike available again.

#### HINTS

- Here's an example: `SET_TO_TRUE_RESULT=$($PSQL "<query_here>")`
- You want to use the `UPDATE`, `SET`, and `WHERE` keywords in the query
- You want to update the `available` column to `true` for the bike with `BIKE_ID_TO_RETURN`
- The query you want is `UPDATE bikes SET available = true WHERE bike_id = $BIKE_ID_TO_RETURN`
- Add `SET_TO_TRUE_RESULT=$($PSQL "UPDATE bikes SET available = true WHERE bike_id = $BIKE_ID_TO_RETURN")` below the `set bike availability to true` comment

## 1730. Add MAIN_MENU Thank you for returning your bike

### 1730.1

After all that is done, send them to the main menu with `Thank you for returning your bike.` as the message.

#### HINTS

- Add the code below the last `send to main menu` comment
- You want to call the `MAIN_MENU` function with the message as an argument
- Here's an example: `MAIN_MENU "<message_here>"`
- Add `MAIN_MENU "Thank you for returning your bike."` below the `send to main menu` comment

## 1740. ./bike-shop.sh

### 1740.1

Run the script and return one of the bikes that `Me` has rented out. When you are done, exit the program.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- The customer with phone number `555-5555` and name `Me` should have at least one rental with the `date_returned` column not null

## 1750. psql SELECT * FROM rentals

### 1750.1

In the psql prompt, view all the data in the `rentals` table.

#### HINTS

- Use the `SELECT` and `FROM` keywords with `*` to view all the data
- Enter `SELECT * FROM rentals;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1760. psql SELECT * FROM bikes ORDER BY bike_id

### 1760.1

Now the rental has been returned. View all the data in the bikes table in order by their `bike_id`.

#### HINTS

- Use the `SELECT` and `FROM` keywords with `*` to view all the data
- Enter `SELECT * FROM bikes ORDER BY bike_id;` in the psql prompt
- You can type `psql --username=freecodecamp --dbname=bikes` into the terminal to log in to psql if you aren't logged in.

## 1770. ./bike-shop.sh

### 1770.1

And the bike is available again. This is the last step. Run the script once more. Feel free to play around, rent and return some bikes. When you are ready to be done, return all the bikes you rented and exit the program.

#### HINTS

- Enter `./bike-shop.sh` in the terminal and press enter
- All rentals should have a `date_returned` value, and all bikes should have `available` set to `true`


## Input & Output

  Jul/6/2018


  ## Iteration 1 - Reading a CSV File

  You are provided a CSV file which contains usernames and other meta data. Source is in the www folder (data.csv).

  Create a PHP script which does the following;

  - Read provided CSV file with PHP.
  - Create data structure to represent each row as a user.
  - Loop through each user and generate a 9 character length password. Passwords should be unique and difficult to guess.
  - Order the data alphabetically by the first_name column.
  - Export array of usernames to JSON file. For every JSON object, the original columns should exist along with the new password column.
  - Version your project if you can. We will build on your solution and do more filtering.

  **You should not...**

  - Need third party libraries to read CSV files. PHP has many libraries already built in to do parsing.


  ## Iteration 2 - User Management

  You'll be creating two classes.

  1. One to manage the users "User Manager"
  2. One to optionally manage a user entity.
    1. Has properties like first_name, last_name, etc. These should not be public.

  Here are some rules.

  - All classes should exist in their own file.
  - I should able to require these new classes (like you would a library).
  - Namespace your classes
  - SQL queries should be sanitized.

  ```
      require_once('./classes/User.php');
      require_once('./classes/UserManager.php');

      // Set up instance of User Manager
      $userManager = new [NAMESPACE]UserManager(FILENAME);

      // Now I should be able to call functions like this...
      $userManager->outputJSON();
      $userManager->getUser(EMAIL_ADDRESS);
      $userManager->deleteUser(EMAIL_ADDRESS);
      $userManager->getAllUsers();
  ```

  The "program" should do the following:

  - Read/Init function to do the following:
    - Read CSV data.
    - Create objects if needed.
    - Create database if it doesn't exist. Connect as needed.
      - (This will only run once, only 1 database should exist.)
    - Create a table if it doesn't exist. Use it as needed.
      - (This will only run once, only 1 database should exist.)
    - Write all read data to database.
      - If the database exists, assume that you don't need to reinsert data.
  - Output the data to a JSON file
  - I should NOT be able to generate new passwords for your users (this should be handled for me on init/read/whatever).
  - I should be able to insert new users to the table.
  - I should be able to retrieve users by email.

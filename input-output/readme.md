
## Input & Output

  Jul/6/2018

  You are provided a CSV file which contains usernames and other meta data. Download the source here [https://bitbucket.org/nitishn/php-trials/src/master/](https://bitbucket.org/nitishn/php-trials/src/master/).

  Create a PHP script which does the following;

  - Read provided CSV file with PHP.
  - Create data structure to represent each row as a user.
  - Loop through each user and generate a 9 character length password. Passwords should be unique and difficult to guess.
  - Order the data alphabetically by the first_name column.
  - Export array of usernames to JSON file. For every JSON object, the original columns should exist along with the new password column.
  - Version your project if you can. We will build on your solution and do more filtering.

  **You should not...**

  - Need third party libraries to read CSV files. PHP has many libraries already built in to do parsing.

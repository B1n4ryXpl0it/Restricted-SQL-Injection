# Restricted-SQL-Injection

## Disclaimer
_This code is provided for educational purposes only._

_It demonstrates SQL injection techniques, which are illegal if used without explicit permission._

_Unauthorized access to computer systems is a criminal offense._

_Always practice ethical hacking and obtain proper authorization before testing any security vulnerabilities._

_The authors and distributors of this code are not responsible for any misuse or illegal activities conducted with this information._

<br>

## Note:

_A web application you are authorised to test is required to test this script._

<br>

## Screenshots:
![Screenshot 2024-11-05 014511](https://github.com/user-attachments/assets/e45a5504-4479-44a5-b70d-ed7c606b3eb6)

<br>

## Steps on how to automate an SQL Injection Vulnerability is as follows:

#### Step 1: Set up the environment
    Import necessary libraries (requests)
    Define global variables (total_queries, charset, target, needle)

<br>

#### Step 2: Create helper functions
    injected_query(payload): Sends POST request with SQL injection payload
    boolean_query(offset, user_id, character, operator): Constructs boolean-based SQL injection query
    invalid_user(user_id): Checks if a user ID exists
    password_length(user_id): Determines the length of the password hash

<br>

#### Step 3: Implement the linear search function `extract_hash(charset, user_id, password_length)`
    Iterate through each character position and charset
    Use boolean queries to find the correct character

<br>

#### Step 4: Implement the binary search function `extract_hash_bst(charset, user_id, password_length)`
    For each character position, perform a binary search on the charset
    Use boolean queries to narrow down the correct character

<br>

#### Step 5: Create a `total_queries_taken()` function to track and display the number of queries made

<br>

#### Step 6: Implement the main loop
    Prompt for user ID input
    Check if the user exists
    If user exists, extract and display the password hash using both linear and binary search methods
    Display the number of queries for each method
    Handle KeyboardInterrupt to exit the loop

<br>
<hr>

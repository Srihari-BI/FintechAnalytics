Schema

Users
user_id (INT, Primary Key)
first_name (VARCHAR)
last_name (VARCHAR)
email (VARCHAR)
phone_number (VARCHAR)
address (VARCHAR)
created_at (TIMESTAMP)
updated_at (TIMESTAMP)

Accounts
count_id (INT, Primary Key)
user_id (INT, Foreign Key to Users)
account_type (VARCHAR)
balance (DECIMAL)
opened_date (DATE)
status (VARCHAR)
branch_id (INT, Foreign Key to Branches)
created_at (TIMESTAMP)
updated_at (TIMESTAMP)

Transactions
transaction_id (INT, Primary Key)
account_id (INT, Foreign Key to Accounts)
transaction_type (VARCHAR)
amount (DECIMAL)
transaction_date (TIMESTAMP)
description (TEXT)
created_at (TIMESTAMP)
updated_at (TIMESTAMP)

Loans
loan_id (INT, Primary Key)
user_id (INT, Foreign Key to Users)
loan_type (VARCHAR)
principal_amount (DECIMAL)
interest_rate (DECIMAL)
term_months (INT)
status (VARCHAR)
disbursed_date (DATE)
created_at (TIMESTAMP)
updated_at (TIMESTAMP)

CreditCards
card_id (INT, Primary Key)
user_id (INT, Foreign Key to Users)
card_type (VARCHAR)
card_number (VARCHAR)
expiration_date (DATE)
balance (DECIMAL)
credit_limit (DECIMAL)
status (VARCHAR)
created_at (TIMESTAMP)
updated_at (TIMESTAMP)

Amusement Park Billing System:
This project is a Python + MySQL based management and billing system for an amusement park named The Magic Kingdom. It allows efficient handling of customer details, available games, and generates bills automatically.

Features:
Create and manage tables: Customers, Water_Games, and Land_Games.
Insert and display customer details.
Insert and display available water and land games with age limits and entry fees.
Join tables to check which customers are eligible for certain games.
Generate bills for customers (with GST included).
Delete tables when needed.

Tech Stack:
Programming Language: Python 
Database: MySQL 
Connector: mysql-connector-python

Functions Implemented:
createtables() → Create required tables
insertcust() → Insert customer records
insertwgame() → Insert water games
insertlgame() → Insert land games
display_customers() → Show all customers
display_Watergames() → Show all water games
display_Landgames() → Show all land games
join_tables() → Join customer & game tables
bill() → Generate a bill for a customer
delete_tables() → Delete selected tables

How to Run:
Install MySQL and create a database named Amusement_Park.
Install required Python library:
pip install mysql-connector-python

Update MySQL credentials in the script (host, user, password).

Run the program:

python amusement_park.py

Advantages:
User-friendly and efficient.
Auto-billing with GST calculation.
Easy access to customer and game records.

Limitations
Internet or database connection required.
Table structures cannot be altered once created.

Future Enhancements
Add offers/discounts for specific games and age groups.
Improve table structure modification support.
Enhance UI for better usability.

References:
NCERT Class 12 Computer Science Textbook
Computer Science with Python by Sumita Arora
Python.org
MySQL.org

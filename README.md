AWS EC2 Login System Project
Overview

This project is a simple full-stack login system deployed on an AWS EC2 Ubuntu server. It uses PHP for backend logic, Apache as the web server, and MySQL as the database.

The goal of this project is to learn how to deploy and manage a working web application in a real cloud environment using AWS.

Architecture
AWS EC2 (Ubuntu Server) – Hosts the application
Apache2 – Web server handling HTTP requests
PHP – Backend logic for authentication
MySQL – Database storing user credentials
SSH (Key-based access) – Remote server management
Features
User login system (login.php)
Email/password authentication
Database connection between PHP and MySQL
API testing using browser and Postman
Deployed and running on a public EC2 IP address
How It Works
User sends login request (browser or Postman)
Request hits login.php on the EC2 server
PHP validates input (email + password)
PHP queries MySQL database
Server returns success or failure response
AWS Setup
EC2 Instance
Ubuntu Server running on AWS EC2
Public IP used to access application
SSH access using .pem key file
Security Groups
Port 22 – SSH access
Port 80 – HTTP web traffic (Apache)
Port 443 – HTTPS (optional)
Database Setup
MySQL installed on EC2
Database connection configured in PHP file (db.php)
Users table stores login credentials

Example fields:

id
email
password
Key Files
login.php – Handles login requests
db.php – Database connection
/var/www/html/ – Apache web root directory
Testing
Browser Test

http://44.195.237.167/login.php

Postman Test

Method: POST
URL: http://44.195.237.167/login.php

Body:

email
password
Security Notes
SSH access restricted via .pem key
Database credentials stored server-side only
Security groups limit open ports
Basic input validation included
What I Learned
Deploying applications on AWS EC2
Linux server management (Ubuntu)
Connecting PHP to MySQL
Using SSH for remote server access
Debugging server issues (500 errors, database issues)
Testing APIs using Postman
Known Issues / Debugging
Occasional 500 Internal Server Error during setup
Database connection issues when credentials change
File permission issues in /var/www/html
Future Improvements
Add password hashing (bcrypt)
Build user registration system
Improve API responses (JSON format)
Move database to AWS RDS
Add HTTPS with SSL (Let’s Encrypt)
Add frontend UI for login page
License

This project is for learning and educational purposes only.

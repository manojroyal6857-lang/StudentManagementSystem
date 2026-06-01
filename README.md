# Student Management System (Java + SQL)

## Overview
A simple console-based application built using Java and MySQL.  
Demonstrates Object-Oriented Programming (OOP) and SQL CRUD operations.

## Features
- Add new students
- View all students
- Menu-driven interface

## Setup
1. Create MySQL database:
   ```sql
   CREATE DATABASE studentdb;
   USE studentdb;
   CREATE TABLE students (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(50),
       age INT,
       course VARCHAR(50)
   );

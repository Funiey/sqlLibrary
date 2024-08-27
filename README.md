# sqlLibrary
# README for SQLite Database

## Overview
This README provides information about a sample SQLite database designed for managing a collection of authors and their respective books. The database includes tables for authors and books, establishing a relationship between them via foreign keys.

## Database Structure

### Tables

1. **Authors Table**
   
    - **Description**: This table stores information about different authors.
      
    - **Schema**:
      
        ```sql

        CREATE TABLE "Authors" (
            "FirstName" TEXT NOT NULL,
        
            "LastName" TEXT NOT NULL,
        
            "Nationality" TEXT NOT NULL,

        
            "AuthorID" INTEGER NOT NULL,
            PRIMARY KEY("AuthorID" AUTOINCREMENT)
        )
  
    - **Fields**:
        - `FirstName`: First name of the author (Text, Not Null)
          
        - `LastName`: Last name of the author (Text, Not Null)
          
        - `Nationality`: Nationality of the author (Text, Not Null)
          
        - `AuthorID`: Unique identifier for each author (Integer, Not Null, Primary Key)

3. **Books Table**
4. 
    - **Description**: This table contains a list of books along with their details.
    - 
    - **Schema**:
        sql
      
        CREATE TABLE "Books" (
            "Title" TEXT NOT NULL,
  
            "BookID" INTEGER NOT NULL,
      
            "AuthorID" INTEGER NOT NULL,
      
            "Description" TEXT,
      
            PRIMARY KEY("BookID" AUTOINCREMENT),
      
            CONSTRAINT "AuthorID" FOREIGN KEY("AuthorID") REFERENCES "Authors"("AuthorID")
        )
      
    - **Fields**:
        - `Title`: Title of the book (Text, Not Null)
          
        - `BookID`: Unique identifier for each book (Integer, Not Null, Primary Key)
          
        - `AuthorID`: Identifier of the author of the book (Integer, Not Null

    - **Author**
   
   Funani Maitakhole
   

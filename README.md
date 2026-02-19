# MongoDB Student Database System

**Course:** Advanced Database IT 4153  
**Student:** Sadaya Preston  
**Project:** Lab 11 - MongoDB Student Database Management

## Project Overview

NoSQL database system designed for managing student records and academic performance data using MongoDB. This project demonstrates proficiency in MongoDB shell commands, document-based data structures, and NoSQL query operations.

## Features

- Student record management using MongoDB
- Performance tracking across multiple assessment types (exams, quizzes, homework)
- Complex queries for data filtering and analysis
- Document-based data structure with nested arrays
- Aggregation and sorting capabilities

## Technologies Used

- **MongoDB** (v7.0.19) - NoSQL database
- **MongoDB Shell** - Command-line interface
- **Homebrew** - Package manager for MongoDB installation
- **macOS Terminal** - Command execution environment

## Database Structure

### StudentDB Collection
The database contains student documents with the following structure:

json
{
  "_id": 5,
  "name": "Student Name",
  "scores": [
    { "score": 44.87, "type": "exam" },
    { "score": 25.72, "type": "quiz" },
    { "score": 63.42, "type": "homework" }
  ]
}


### Key Features:
- Each student has a unique `_id`
- Student names are stored as strings
- Scores are stored in an array of subdocuments
- Each score has a `type` (exam, quiz, homework) and numeric `score` value

## Installation & Setup

### Prerequisites
- macOS (or Linux/Windows with MongoDB installed)
- MongoDB installed via Homebrew

### Installation Steps

1. **Install MongoDB using Homebrew:**
     bash
   brew install mongodb-community@7.0
   

2. **Start MongoDB service:**
     bash
   brew services start mongodb/brew/mongodb-community@7.0
   

3. **Connect to MongoDB:**
     bash
   mongosh
   

4. **Switch to StudentDB:**
     javascript
   use StudentDB
   

## Key Queries Implemented

### Basic Operations
  javascript
// View all students
db.students.find()

// View all students with formatted output
db.students.find().pretty()

// Find one student
db.students.findOne()
```

### Filtering & Analysis
```javascript
// Find specific student by name
db.students.find({ name: "Wilburn Spiess" }).pretty()

// Find students with specific criteria
// (See queries/mongodb_queries.txt for complete list)
```

### Data Analysis
  javascript
// Count total students
db.students.count()

// Sort students by name
db.students.find().sort({ name: 1 })


## Screenshots

Screenshots show:
1. MongoDB installation and setup
2. Database connection and initialization
3. Student data queries and retrieval
4. Data filtering and analysis
5. Query results with `.pretty()` formatting

## See `/screenshots` folder for detailed visual documentation.

## What I Learned:

### Technical Skills
- **NoSQL Database Design:** Understanding document-based data structures vs relational tables
- **MongoDB Query Syntax:** Writing queries using MongoDB's JSON-like syntax
- **Data Modeling:** Storing nested data using arrays and subdocuments
- **Command Line Proficiency:** Using MongoDB shell for database operations

### Key Concepts
- Difference between SQL and NoSQL approaches
- When to use document-based databases
- Flexibility of schema-less design
- Working with nested data structures
- Query optimization in MongoDB

### Challenges Overcome
- Installing and configuring MongoDB on macOS
- Understanding MongoDB's document structure
- Navigating between databases (`use StudentDB`, `use Sprest11`)
- Formatting query outputs for readability

## 🔧 Lab Requirements Met

- Successfully installed MongoDB
- Connected to MongoDB database
- Executed basic find() operations
- Used findOne() for single document retrieval
- Filtered students by various criteria
- Displayed results with pretty formatting
- Documented all queries with screenshots

## Course Information

**Institution:** Kennesaw State University  
**Major:** Information Technology (Data Analytics Concentration)  
**Course:** IT 4153 - Advanced Database  
**Lab Assignment:** Lab 11 - MongoDB Student Database

## Author

**Sadaya Preston**
- GitHub: [@xsadaya](https://github.com/xsadaya)
- LinkedIn: [Sadaya Preston](https://www.linkedin.com/in/sadaya-preston-245305230)
- Portfolio: [xsadaya.github.io](https://xsadaya.github.io)




---

**Note:** This project demonstrates academic work in database management and NoSQL concepts. All student data used is sample/fictional data for educational purposes.

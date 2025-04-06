"I'm thrilled to share my very first project on GitHub!
I chose this platform to share my knowledge, receive constructive feedback if there are any mistakes, learn from them, and continuously improve by posting upgraded versions. I'm excited to grow and contribute through this journey."
"I’m passionate about transitioning my career into Data Science.
As I began exploring this field, I realized how important it is to understand data — how it works, how to analyze it, and how to handle it efficiently. This project is one of my first steps toward gaining practical experience in data handling and analysis."
"As a first step in my Data Science journey, I started learning SQL.
SQL introduced me to databases, where multiple tables are stored. These tables are often connected to each other through various relationships.
Understanding these relationships clearly helped me write efficient SQL queries, perform table joins, and extract meaningful insights from the data. This foundational knowledge is essential for any data-driven role, and it has been an exciting learning experience for me."
📁 Repository & Project
As part of my learning journey, I created a repository called bokk, where I’ve added a project named gravity_books.

This project is inspired by and based on resources from @bbrumm/databasestar, a great source for understanding SQL and database structures. I’ve used the materials provided there to practice SQL queries, understand table relationships, and explore how data is managed in real-world scenarios.
Before jumping into writing SQL queries, I began by carefully studying the ER (Entity-Relationship) Diagram of the database.

The ER diagram helped me understand:

What tables are available in the database

What each table represents

How the tables are related to one another (via primary and foreign keys)

The one-to-many or many-to-one relationships between tables

This foundational step gave me a clear view of the database structure, making it easier to write accurate and meaningful queries later on.
🔗 Exploring Table Relationships: book and publisher
To begin understanding the database, I started with the two connected tables: book and publisher.

📘 book Table
This table stores detailed information about each book, including:

book_id (Primary Key)

title

isbn13

language_id

num_pages

publication_date

publisher_id (Foreign Key)

🏢 publisher Table
This table holds information about book publishers:

publisher_id (Primary Key)

publisher_name

🔄 Relationship Between book and publisher
Each book is published by one publisher.

One publisher can publish multiple books.

This forms a one-to-many relationship:

One publisher → Many books

Linked by the publisher_id field in both tables

🔍 What I Learned
Understanding this relationship helped me:

Write JOIN queries to combine data from both tables

Extract meaningful insights like:

List of books published by a particular publisher

Count of books per publisher
📘 Deep Dive: More Relationships Around the book Table
After exploring the relationship between book and publisher, I moved on to see how the book table connects with other entities like authors and languages.

🧾 Tables Involved
book – Contains book information

book_author – A junction table connecting books and authors (many-to-many)

author – Contains author names and IDs

book_language – Stores the language details of each book

📚 book ↔ author (Many-to-Many Relationship)
One book can have multiple authors

One author can write multiple books

To handle this many-to-many relationship, we use the intermediate table book_author, which contains:

book_id

author_id

This allows flexible mapping between books and authors.

🌐 book ↔ book_language (Many-to-One Relationship)
Each book is written in one language (represented by language_id)

One language can apply to many books

The language_id in the book table links to the book_language table, which includes:

language_code

language_name

Example: A book with language_id = 1 might correspond to English in the book_language table.

🔍 What I Gained from This
Learned how to handle many-to-many relationships using a junction table (book_author)

Practiced JOINs across 3-4 tables

Understood the importance of foreign keys in maintaining database integrity

Became more confident in designing SQL queries for real-world data relationships



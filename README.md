# Chatbot – PHP & MySQL

A simple **web-based chatbot application** developed using **HTML, CSS, JavaScript, PHP, and MySQL**. The chatbot allows users to interact through a web interface and retrieves appropriate responses from a MySQL database.

The project also includes an **admin interface** for storing chatbot queries and replies in the database.

## Project Overview

This project demonstrates the implementation of a rule/database-based chatbot using a PHP backend and MySQL database.

Users can enter questions or messages through the chatbot interface. The input is sent to the PHP backend using **AJAX**, which processes the request and returns a response that is displayed dynamically in the chat window.

The project also provides an admin section where new **queries and replies** can be added to the chatbot database.

##  Features

* 💬 Interactive chatbot interface
* 🔄 Real-time communication using AJAX
* 🗄️ MySQL database integration
* 👨‍💻 Admin interface for adding chatbot responses
* 📝 Stores user queries and chatbot replies
* 🔊 Text-to-speech functionality
* 📱 Responsive web interface
* ⚡ Dynamic chat messages without page reload
* 🔐 Admin login interface

The chatbot frontend contains an input field and Send button, and sends the entered text to `message.php` using a POST AJAX request.

## 🛠️ Technologies Used

| Technology     | Purpose                   |
| -------------- | ------------------------- |
| HTML5          | Web page structure        |
| CSS3           | User interface styling    |
| JavaScript     | Client-side functionality |
| jQuery         | AJAX communication        |
| PHP            | Backend processing        |
| MySQL          | Database storage          |
| PDO            | Database connectivity     |
| Web Speech API | Text-to-speech            |

## Project Structure

```text
Chatbot/
│
├── bot.php
├── admin.php
├── data.php
├── message.php
├── insert.php
├── login.html
├── style.css
├── bot.png
├── database.php
└── README.md
```

> Additional files such as `message.php`, `insert.php`, `login.html`, `style.css`, and `bot.png` are referenced by the uploaded project files.

## How It Works

```text
        ┌─────────────────┐
        │      User       │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Chatbot UI      │
        │    bot.php      │
        └────────┬────────┘
                 │
                 │ AJAX POST
                 ▼
        ┌─────────────────┐
        │   message.php   │
        │ Backend Logic   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  MySQL Database  │
        │      bot        │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Chatbot Reply   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Display Reply   │
        │   to User       │
        └─────────────────┘
```

## Database

The chatbot uses a MySQL database containing a `bot` table.

The application retrieves fields including:

```text
id
queries
replies
```

The admin page provides fields for entering a chatbot **query** and its corresponding **reply**, which are submitted to `insert.php`.

## Admin Panel

The admin section allows administrators to add new chatbot knowledge to the database.

### Admin workflow

```text
Admin Login
     ↓
Admin Panel
     ↓
Enter Query
     ↓
Enter Reply
     ↓
Submit
     ↓
Store in MySQL
```

The stored chatbot records can also be displayed in a table from the database.

## Text-to-Speech

The chatbot includes browser-based text-to-speech using the JavaScript `speechSynthesis` API.

The implementation uses:

```javascript
window.speechSynthesis
```

and configures the voice language as:

```text
en-IN
```

This allows chatbot responses to be converted into spoken output.

## Requirements

Before running the project, install:

* PHP 7.x or later
* MySQL
* Apache Server
* XAMPP / WAMP / LAMP
* Modern web browser

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/chatbot.git
```

### 2. Move the project

For XAMPP:

```text
C:\xampp\htdocs\chatbot
```

### 3. Start Apache and MySQL

Open XAMPP Control Panel and start:

```text
Apache
MySQL
```

### 4. Create the database

Create a MySQL database and a table named:

```text
bot
```

with fields similar to:

```text
id
queries
replies
```

### 5. Configure the database

Update the database connection settings in the PHP files according to your local MySQL configuration.

**Important:** Do not upload database passwords or other credentials to GitHub. Use environment variables or a separate configuration file.

### 6. Run the application

Open:

```text
http://localhost/chatbot/bot.php
```

## Example

### User

```text
Hi
```

### Chatbot

```text
Hello! How can I help you?
```

The chatbot starts with a greeting message in the interface and dynamically appends user and bot messages during the conversation.

## Security Note

**Never commit database credentials to GitHub.**

The uploaded PHP files currently contain database connection credentials directly in the source code.

Before publishing this project publicly:

1. Remove the real database username and password.
2. Change the database password if it has been exposed.
3. Add sensitive configuration files to `.gitignore`.
4. Use environment variables for production credentials.

Example:

```text
.env
config.php
```

Add them to `.gitignore` where appropriate.

## Future Improvements

* Add Natural Language Processing (NLP)
* Implement machine-learning-based response generation
* Add user authentication
* Improve admin dashboard
* Add chatbot conversation history
* Add voice input
* Improve database security
* Add REST API support
* Deploy the chatbot to a cloud server
* Improve UI/UX and mobile responsiveness

##  Project Type

**Academic Project – Project Work Phase II**

### Project Title

**Implementation of Chatbot**

## Author

**Vijay Kumar M R**

Artificial Intelligence & Machine Learning

## License

This project is intended for educational and academic purposes. You may modify and extend the project for learning and development.

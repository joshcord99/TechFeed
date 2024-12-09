
# Just Tech News

**Just Tech News** is a Python-powered web application that allows users to submit tech-related articles, comment on articles, and upvote them.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Setup](#setup)
- [Development Workflow](#development-workflow)
- [Technologies Used](#technologies-used)
- [Routes](#routes)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## Overview

The app provides a platform for tech enthusiasts to:
- Submit links to tech-related articles.
- Comment on others' articles.
- Upvote articles to give them more visibility.

This project demonstrates how to utilize Python and Flask for a back-end application.

---

## Features

- **User Authentication**: Sign up, log in, and log out functionality.
- **Content Management**: Post articles, edit posts, and leave comments.
- **Voting System**: Upvote articles for visibility.
- **Dynamic Templating**: Jinja2 templates for rendering HTML pages with data.

---

## Setup

Follow these steps to set up the project:

### Prerequisites
- Python 3.8+ installed
- MySQL installed and configured
- Virtual Environment (venv) enabled

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/joshcord99/python-newsfeed.git
   cd python-newsfeed
   ```

2. **Set Up a Virtual Environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # For macOS/Linux
   .\venv\Scripts\activate   # For Windows
   ```

3. **Install Dependencies**:
   ```bash
   pip install flask flask-sqlalchemy flask-session
   ```

4. **Configure the Database**:
   - Create a MySQL database.
   - Add your database credentials to a `.env` file:
     ```
     DB_URL=mysql+pymysql://username:password@localhost/python_newsfeed
     SECRET_KEY=super_secret_key
     ```

5. **Run the App**:
   ```bash
   python -m flask run
   ```

6. **Access the App**:
   Visit `http://127.0.0.1:5000` in your browser.

---

## Development Workflow

### Git Workflow
1. Create a new branch for each feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Commit and push changes to GitHub:
   ```bash
   git add .
   git commit -m "Add feature"
   git push origin feature/your-feature-name
   ```
3. Create a pull request and merge it into the `main` branch after review.

---

## Technologies Used

- **Python**: Back-end programming language.
- **Flask**: Web framework for building routes and serving templates.
- **SQLAlchemy**: ORM for database management.
- **Jinja2**: Template engine for rendering dynamic HTML.
- **MySQL**: Relational database for storing user and content data.

---

## Routes

### Public Routes
| Route          | HTTP Method | Description                |
|-----------------|-------------|----------------------------|
| `/`            | GET         | Homepage                  |
| `/login`       | GET         | Login page                |
| `/post/<id>`   | GET         | View a single post        |

### Dashboard Routes
| Route                | HTTP Method | Description                |
|-----------------------|-------------|----------------------------|
| `/dashboard`         | GET         | Dashboard homepage         |
| `/dashboard/edit/<id>`| GET         | Edit a post                |

### API Routes
| Route          | HTTP Method | Description                |
|-----------------|-------------|----------------------------|
| `/api/users`    | POST        | Sign up a new user         |
| `/api/users/login`| POST      | Log in a user             |
| `/api/users/logout`| POST     | Log out a user            |
| `/api/comments` | POST        | Add a new comment         |

---

## Future Enhancements

- **User Profiles**: Add personalized user profiles.
- **Search Functionality**: Allow users to search for posts by keywords.
- **Enhanced Security**: Implement OAuth for third-party logins.

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

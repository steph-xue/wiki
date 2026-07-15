# Wiki

A full stack encyclopedia web application, inspired by Wikipedia, where users can browse, search, create, edit, and delete entries. Each entry is written in Markdown and rendered as a formatted web page, and a persistent sidebar makes it easy to search or move between pages from anywhere on the site.

<br>

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Getting Started](#getting-started)
- [Future Improvements](#future-improvements)

<br>

## Overview

This project recreates the core experience of an online encyclopedia. The frontend is built with HTML5, CSS3, and Bootstrap, presenting a clean two column layout with a fixed sidebar for navigation and search alongside a main content area. The backend is built with Django and Python, and handles routing, searching, and page creation. Encyclopedia entries are stored as individual Markdown files, and the Markdown library converts them into HTML for display, so content can be written using simple Markdown syntax rather than raw HTML.

<br>

## Features

### Homepage
The homepage lists every encyclopedia entry in alphabetical order, with each title linking directly to its page. This gives users a clear view of everything available and lets them open any entry with a single click.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/homepage.png?raw=true" alt="Homepage" width="700"></p>

<br>

### Navigation Sidebar
A sidebar stays visible on every page and serves as the main way to move around the application. It includes a search bar for finding entries, a link to the homepage, a link to create a new page, and a link that takes the user to a random entry.

<br>

### Wiki Entry
Each entry page displays the title along with the fully rendered content of the entry. Two actions are available directly on the page. Edit opens the entry in an editable form so the title and content can be updated and saved, while Delete removes the entry entirely and returns the user to the homepage.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/wiki_entry.png?raw=true" alt="Wiki Entry" width="700"></p>

<br>

### Search
The search bar supports two behaviors. If the query exactly matches an entry title, the user is taken straight to that entry. If it does not, the application returns a list of every entry whose title contains the query as a substring, making it easy to find related pages even without the exact name.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/search_results.png?raw=true" alt="Search Results" width="700"></p>

<br>

### Create New Entry
Users can add a new page by providing a title and content written in Markdown. If an entry with the same title already exists, the application displays an error to prevent duplicates. Otherwise the new entry is saved and the user is taken directly to its finished page.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/create_entry.png?raw=true" alt="Create New Entry" width="700"></p>

<br>

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | HTML5, CSS3, Bootstrap |
| Backend | Django, Python, Markdown |
| Storage | Local file system |

<br>

## How It Works

Every page in the application extends a shared Bootstrap layout, which keeps the sidebar and overall structure consistent while only the main content changes from page to page. On the backend, Django routes each request to the matching view. Depending on the action, that view reads, creates, updates, or deletes the relevant Markdown file, converts its contents from Markdown into HTML using the Python Markdown library, and renders the result with the appropriate template. Storing entries as plain Markdown files keeps the content simple to manage and easy to edit both inside and outside the application.

<br>

## Getting Started

Follow the steps below to set up and run the application on your own machine.

**Prerequisites**

Make sure Python 3 is installed before you begin. You can check by running the command below, which should print a version number.
```bash
python --version
```

**1. Clone the repository**

This downloads a copy of the project to your computer and moves you into the project folder.
```bash
git clone https://github.com/steph-xue/wiki.git
cd wiki
```

**2. Create and activate a virtual environment (recommended)**

This keeps the project's dependencies separate from other Python projects on your machine.
```bash
python3 -m venv venv
source venv/bin/activate      # On Windows use: venv\Scripts\activate
```

**3. Install the dependencies**

This installs Django and the Markdown library the project needs to run.
```bash
pip install -r requirements.txt
```

**4. Set up the database**

This prepares the local database Django uses for sessions and administration.
```bash
python3 manage.py makemigrations
python3 manage.py migrate
```

**5. Start the development server**

This runs the application locally.
```bash
python3 manage.py runserver
```

Once the server is running, open `http://127.0.0.1:8000/` in your browser to start using the application.

<br>

## Future Improvements
Several enhancements are planned to extend the functionality of the application:
- User accounts so new pages and edits can be attributed to contributors
- Page history so changes to an entry can be tracked and reverted
- A live preview of Markdown while creating or editing an entry
- A live hosted demo to allow users to try the application without a local setup

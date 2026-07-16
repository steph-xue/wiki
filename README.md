
<h1 align="center">
  Wiki
</h1>

<h4 align="center">
  A full-stack encyclopedia web application, inspired by Wikipedia, where users can browse, search, create, edit, and delete wiki entries.
</h4>

<p align="center">
  <img src="/encyclopedia/static/encyclopedia/images/homepage.png?raw=true" alt="Homepage" width="500">
</p>

<br>

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Future Improvements](#future-improvements)
- [Getting Started](#getting-started)

<br>

## Overview

This project is a full-stack encyclopedia web application that allows users to browse, search, create, edit, and delete wiki entries. The frontend is built with HTML, CSS, and Bootstrap and uses a clean two-column layout with a persistent sidebar for navigation and search alongside the main content area. The backend is built with Python and Django and handles routing, searching, and page management. Each wiki entry is stored as an individual Markdown file, and the Markdown library converts the content into formatted HTML for display in the browser, allowing entries to be written using simple Markdown syntax rather than raw HTML.

<br>

## Features

### Homepage and Navigation
The homepage lists every wiki entry in alphabetical order, with each title linking directly to its own page. A sidebar stays visible on every page and serves as the main way to move around the application. It includes a search bar labeled "Search Encyclopedia," a "Home" link back to the entry list, a "Create New Page" link for adding a new entry, and a "Random Page" link that takes the user directly to a randomly selected entry, offering a quick way to explore the encyclopedia.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/homepage.png?raw=true" alt="Homepage" width="700"></p>

<br>

### Wiki Entry
Each wiki entry page displays the title along with the fully rendered content of the entry, converted from Markdown into formatted HTML. Two actions are available directly on the page. Edit opens a form prefilled with the entry's existing title and content so it can be updated and saved, while Delete removes the entry's underlying file entirely and returns the user to the homepage. If a requested entry does not exist, the application displays an error page rather than a broken link.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/wiki_entry.png?raw=true" alt="Wiki Entry" width="700"></p>

<br>

### Search
The search bar in the sidebar supports two behaviors. If the query exactly matches a wiki entry title, the user is taken straight to that entry's page. If it does not, the application performs a case insensitive substring match and returns a list of every wiki entry whose title contains the query, with each result linking to its own entry, making it easy to find related pages even without knowing the exact name.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/search_results.png?raw=true" alt="Search Results" width="700"></p>

<br>

### Create New Entry
Users can add a new wiki entry from the "Create New Page" link by providing a title and content written in Markdown. Before saving, the application checks whether an entry with the same title already exists and displays an error message to prevent duplicates if it does. Otherwise the new entry is saved as a Markdown file and the user is taken directly to its finished, rendered page.

<p align="center"><img src="/encyclopedia/static/encyclopedia/images/create_entry.png?raw=true" alt="Create New Entry" width="700"></p>

<br>

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | HTML, CSS, Bootstrap |
| Backend | Django, Python |
| Libraries | Markdown (converts Markdown content of each wiki entry into HTML for display) |
| Storage | Local file system |
  
<br>

## How It Works

Each page renders within a two column Bootstrap layout, where the sidebar handles search and navigation while the main panel displays whichever entry, search results, or form is currently active. On the backend, Django routes each incoming request to the view that matches the action being performed, whether that means reading, creating, updating, or deleting a wiki entry. That view handles the corresponding Markdown file directly, converting its contents into HTML using the Python Markdown library before rendering the result with the appropriate template. Search queries are matched against entry titles first for an exact match, and if none is found, a case insensitive substring match is used to build a list of related results. Storing wiki entries as plain Markdown files on the local file system keeps the content simple to manage and easy to edit both inside and outside the application.

<br>

## Future Improvements
Several enhancements are planned to extend the functionality of the application:
- User accounts so new pages and edits can be attributed to contributors
- Page history so changes to an entry can be tracked and reverted
- A live preview of Markdown while creating or editing an entry
- A live hosted demo to allow users to try the application without a local setup

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

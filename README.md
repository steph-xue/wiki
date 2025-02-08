# Wiki Project
The wiki project allows the user to view, search, edit, and create encyclopedia entries on a wikipedia-based web application.
<br></br>


## Encyclopedia App

**Homepage**
- The user can view the list of encyclopedia entries on the homepage with links to each of the entries (displayed in alphabetical order)
- Clicking on the associated link allows the user to view the encyclopedia entry details
&nbsp;

![Homepage](/encyclopedia/static/encyclopedia/images/homepage.png?raw=true "Homepage")
<br></br>

**Navigation Sidebar**
- The navigation sidebar allows the user to search for encyclopedia entries, go to the homepage, create a new entry, or go to a random entry
    - The search bar allows the user to search the full name of the entry (gives the entry page) or sub-string (gives a list of search results containing the substring)
    - The homepage displays the list of all encyclopedia entries
    - Creating a new entry allows the user to create and save a new entry (title and description)
    - Random entry brings the user to a random encyclopedia entry page
<br></br>

**Wiki Entry**
- Each encyclopedia entry will allow the user to view details of the entry, make edits (to the title or description) and save the edits
&nbsp;

![Wiki Entry](/encyclopedia/static/encyclopedia/images/wiki_entry.png?raw=true "Wiki Entry")
<br></br>

**Search Results**
- The search bar allows the user to search the full name of the entry (gives the entry page) or sub-string (gives a list of search results containing the substring)
&nbsp;

![Search Results](/encyclopedia/static/encyclopedia/images/search_results.png?raw=true "Search Results")
<br></br>

**Create New Entry**
- Creating a new entry allows the user to create and save a new entry (must provide a title and description)
&nbsp;

![Create New Entry](/encyclopedia/static/encyclopedia/images/create_entry.png?raw=true "Create New Entry")
<br></br>

## Languages & Frameworks
- The wiki project was created using Django, a Python-based web framework
- JavaScript was utilized to create a single-page web application with dynamic user interfaces

## How to Run Locally
- Install the latest version of python
    - Check the version using the command
        - ```python --version```
- Clone the repository from github by typing in the command line
    - ```git clone <repo-url>```
- Install any dependencies by using the command
    - ```pip install -r requirements.txt```
- Apply database migrations by typing in the command line
    - ```python manage.py migrate```
- The web application can be run on your local server by typing the command
    - ```python3 manage.py runserver```
  


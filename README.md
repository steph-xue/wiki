# Wiki Project
The wiki project allows the user to view, search, edit, and create encyclopedia entries on a wikipedia-based web application.

## Encyclopedia App
- The user can view the list of encyclopedia entries on the homepage with links to each of the entries (displayed in alphabetical order)
- Clicking on the associated link allows the user to view the encyclopedia entry (title, description, can make edits)
    - Each encyclopedia entry will allow the user to make edits (to the title or description) and save the edits
- The navigation sidebar allows the user to search for encyclopedia entries, go to the homepage, create a new entry, or go to a random entry
    - The search bar allows the user to search the full name of the entry (gives the entry page) or sub-string (gives a list of search results containing the substring)
    - The homepage displays the list of all encyclopedia entries
    - Creating a new entry allows the user to create and save a new entry (title and description)
    - Random entry brings the user to a random encyclopedia entry page

## Specifications and How to Run
- The wiki project was created using Django, a Python-based web framework
- The web application can be run in the terminal using 'python3 manage.py runserver'
  
&nbsp;  

# Example Images
## Homepage
![Homepage](/encyclopedia/static/encyclopedia/images/homepage.png?raw=true "Homepage")
The homepage contains links to each of the wiki entries displayed in alphabetical order.

## Wiki Entry
![Wiki Entry](/encyclopedia/static/encyclopedia/images/wiki_entry.png?raw=true "Wiki Entry")
Each encyclopedia entry displays a title and the associated written description. Users can make and save edits to any wiki entries.

## Search Results
![Search Results](/encyclopedia/static/encyclopedia/images/search_results.png?raw=true "Search Results")
The search bar allows the user to search the full name of the entry (gives the entry page) or sub-string (gives a list of search results containing the substring).

## Create New Entry
![Create New Entry](/encyclopedia/static/encyclopedia/images/create_entry.png?raw=true "Create New Entry")
Creating a new entry allows the user to create and save a new entry.

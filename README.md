# CS50---Project-5---Capstone
A to-do List website built using HTML, CSS, Django, Python and Javascript.

Features of this app include:
- Creating lists
- Creating and editing list items inside each list
- Following other users created lsits
- Pagination
- Editing lists
- Marking list items as complete

Distinctiveness and Complexity:
This project contains multiple aspects across all the different projects of this course aswell as some extra. Features such as creating and editing lists, pagination and following other users lists were inspired from the other projects. Additional features which I think add another level of complexity include:
- List Items which are separate models that are attributed to each List, the List Items can be added or removed from Lists in the 'Edit List' page. Each List has multiple ListItem models associated to it. Adding or removing List Items is done using Javascript and so no page refresh is required to see the changes.
- The 'Category' page which only displays Categories where users have created lists, if a category does not contain any lists then it is not available to select on this page. 
- Marking List Items as complete. Users can mark List-Items as complete by clicking a chekcbox next to each List Item. This Strikes through the text of the List Item and moves the List Item to the bottom of the list using Javascript without requiring a page refresh. User's can un-check the 'completed' box and this marks the List Item as active again, removing the strikethough and un-checking the 'completed' box.

Contents of important files:
- Views.py: This contains the Python code that allows users to create and edit the different models in the project, navigate between pages, and perform some important functions for the site.
- urls.py: Allows the user to navigate to different parts of the site and access different functions.
- models.py: contains the different models used in the app.
- HTML documents include: 'category_individual', 'category_select', 'edit_list', 'follow_view', 'index', 'layout', 'login', 'profile', 'register'. These HTML files are in the 'templates' folder.
- static Folder: this folder contains index.js and styles.css. Index.js is important for running much of this app as I tried to use Javascript where possible. 

Running the application:
The 'lists' folder should contain a folder called 'listsapp' and the manage.py file.
The views.py, urls.py, models.py files should be located under 'lists' -> 'listsapp'
In the same directory, the folders _pycache_, migrations, static & templates should also be located.
Inside the 'templates' folder should be another folder called 'listsapp' which contains all the html documents.
Inside the 'static' folder should be another folder called 'listsapp' which contains index.js and styles.css.
To launch the application, users can cd to the 'lists' directory containing the manage.py file. The user can then run 'py manage.py runserver'.


Here is an overall description of the app:

The first feature is the ability to create lists. Lists have a title, a category which is selected from a drop-down, and can be private or public.
Lists contain 'list-items' which can be added/removed/edited aswell as marked as complete.

The home page contains all 'public' lists from all users, ordered from newest at the top, to oldest at the bottom. At the top of this page, IF the user is logged in, is an option to 'Create a New List'. When the user creates a new list, they're brought to the 'Edit List' page where they can add List Items. If the user adds or deletes a list item, the change is shown without a page update required. Each list item is a model in django and so adding or removing ListItems is performed using Javascript fetch functions to create or remove 'ListItem' models, then update the page without any refresh. Once the user has added all the list items, they can save the list, which will show up on the home page IF it is a public list. If the user created the list, they have the option of editing it or deleting it. Clicking 'Delete' will remove the list and replace it with a message stating 'List item has been deleted', this occurs without requiring a page refresh. This code is written with security and scalability in mind.

The 'Profile' page can be accessed by clicking on the username of a List creator. There is also a button in the top navigation bar to view the user's own profile. In the profile page you see all the PUBLIC lists for that user, if you are viewing your own page, then you will see your own private posts.

The Categories page shows all the categories that contain lists, if a category has no lists in it, then it is not viewable on the Categories page. Users can click into any category and view all the Public lists in that category, if the user has a private list in that category, then ofcourse they can view their own private list. 

User's can Follow other user's lists. The Follow button toggles from 'Follow' to 'Un-Follow' as the user clicks the button, this is done using Javascript. Followed lists are visible in the users 'Followed Lists' page. 

The website uses Pagination where 10 Lists are viewable per page. At the bottom of the page the user can go forward or back pages depending on what page they're on.

User's can mark items as complete. For user's who are logged in, they can mark List items on their own lists as complete by ticking a checkbox. Once clicked, the checkbox toggles to 'ticked', the List Item text gets a strikethrough, and the List Item moves to the bottom of the List. This is performed in Javascript so no page refresh is required. Completed items at the bottom of the list can be un-checked to mark them as active, this removes the Strickthrough, un-checks the box making the List Item active again. 

Thank you for reviewing and I hope you are impressed with my final project! I also would like to say that this course was very well-run, the standard of teaching, the layout of the course and the course material were all to a very high standard. I am thankful that Harvard is giving this out for free to the public.




# CS50---Project-5---Capstone
A to-do List website built using HTML, CSS, Django, Python and Javascript.

Features of this app include:
- Creating lists
- Creating and editing list items inside each list
- Following other users created lsits
- Pagination
- Editing lists
- Marking list items as complete

Thank you for reviewing my final project! I'm very excited to present this and I hope you are impressed!

The first feature is the ability to create lists. Lists have a title, a category which is selected from a drop-down, and can be private or public.
Lists contain 'list-items' which can be added/removed/edited aswell as marked as complete.

The home page contains all 'public' lists from all users, ordered from newest at the top, to oldest at the bottom. At the top of this page, IF the user is logged in, is an option to 'Create a New List'. When the user creates a new list, they're brought to the 'Edit List' page where they can add List Items. If the user adds or deletes a list item, the change is shown without a page update required. Each list item is a model in django and so adding or removing ListItems is performed using Javascript fetch functions to create or remove 'ListItem' models, then update the page without any refresh. Once the user has added all the list items, they can save the list, which will show up on the home page IF it is a public list. If the user created the list, they have the option of editing it or deleting it. Clicking 'Delete' will remove the list and replace it with a message stating 'List item has been deleted', this occurs without requiring a page refresh. This code is written with security and scalability in mind.

The 'Profile' page can be accessed by clicking on the username of a List creator. There is also a button in the top navigation bar to view the user's own profile. In the profile page you see all the PUBLIC lists for that user, if you are viewing your own page, then you will see your own private posts.

The Categories page shows all the categories that contain lists, if a category has no lists in it, then it is not viewable on the Categories page. Users can click into any category and view all the Public lists in that category, if the user has a private list in that category, then ofcourse they can view their own private list. 

User's can Follow other user's lists. The Follow button toggles from 'Follow' to 'Un-Follow' as the user clicks the button, this is done using Javascript. Followed lists are visible in the users 'Followed Lists' page. 

The website uses Pagination where 10 Lists are viewable per page. At the bottom of the page the user can go forward or back pages depending on what page they're on.

User's can mark items as complete. For user's who are logged in, they can mark List items on their own lists as complete by ticking a checkbox. Once clicked, the checkbox toggles to 'ticked', the List Item text gets a strikethrough, and the List Item moves to the bottom of the List. This is performed in Javascript so no page refresh is required. Completed items at the bottom of the list can be un-checked to mark them as active, this removes the Strickthrough, un-checks the box making the List Item active again. 

Thank you for reviewing and I hope you are impressed with my final project! I also would like to say that this course was very well-run, the standard of teaching, the layout of the course and the course material were all to a very high standard. I am thankful that Harvard is giving this out for free to the public.




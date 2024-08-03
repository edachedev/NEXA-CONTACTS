GROUP NAME: BINARY BOSSES
PROJECT TITLE: CONTACT MANAGEMENT SYSTEM (NEXA CONTACTS)
	NAME OF GROUP MEMBERS	MATRIC NUMBER	GITHUB USER
1.	EDACHE VICTOR OWOICHO  	BHU/23/04/05/0073    	EDACHEDEV
2.	GABRIEL .I. DIVINE	BHU/23/04/05/0112	D1V1NEE
3.	OJO .E. OLUWATOBI                 	BHU/23/04/05/0108	EZERELO
4.	IHUWE KATER SILAS	BHU/23/04/09/0085	IHUWE
5.	MUKHTAR YUSUF                      	BHU/23/04/09/0052	MUKTYY


PROJECT DESCRIPTION
Description:
The Contact Management System is a web application designed to streamline the management of contact information. Leveraging the Model-View-Controller (MVC) design pattern, the application offers a robust and user-friendly interface for managing contact details effectively.

KEY FEATURES:
Create: Add new contacts with name, phone number, and email.
Read: View a list of all contacts.
Update: Edit existing contact details.
Delete: Remove contacts from the system.

Add Contacts: Users can easily add new contacts by inputting essential details such as names, phone numbers, email addresses, and physical addresses. The system ensures that all information is stored accurately and is readily accessible.
 
Edit Contacts: Users can update existing contact information to keep it current. Changes can be made to any detail, allowing for effective management of contact data as it evolves.

 
Read Contacts: The application provides an intuitive interface to view and search through contact details. Users can quickly locate specific contacts and review their information in a structured format.
 

Delete Contacts: Users have the option to remove contacts from the system. This feature ensures that outdated or unnecessary information can be easily deleted, keeping the contact database clean and relevant.
 
Technology Stack:
Backend: Python Flask
Database: SQLite (using SQLAlchemy)
Frontend: HTML, CSS
Backend: Python-based server to manage data operations and business logic.
Frontend: A web-based interface designed for ease of use and visual appeal.
Database: Structured storage for efficiently managing and accessing contact data.
Purpose:
The system is designed to enhance organizational efficiency by providing comprehensive tools for managing contact information. It ensures that users can add, update, view, and delete contacts with ease, facilitating better communication and relationship management.


NAME: EDACHE VICTOR OWOICHO
MATRIC NUMBER: BHU/23/04/05/0073 
GITHUB USER NAME: EDACHEDEV
Introduction:
 I’ll be describing how I used Python Flask to design the backend of my contact management application. Flask is a lightweight web framework that allows for rapid development of web applications, making it an excellent choice for this project.
1. Setting Up Flask:
I started by importing the necessary modules: Flask for creating the web application, request for handling incoming data, redirect and url_for for routing, and render_template for rendering HTML templates.
2. Application Configuration:
Next, I initialized the Flask application with app = Flask(__name__). I then configured the application to use a SQLite database by setting SQLALCHEMY_DATABASE_URI and disabled modification tracking to optimize performance.
3. Database Initialization:
I used db.init_app(app) to bind the database to the Flask application. The create_tables function, which is executed before every request, ensures that all the necessary tables are created in the database.
4. Routing and Views:
Home Route:
The / route retrieves all contacts from the database using Contact.query.all() and renders the home.html template to display them.
Add Contact Route:
The /add route handles both GET and POST requests. For GET requests, it renders the add_contacts.html form. For POST requests, it collects the contact details from the form, creates a new Contact object, and saves it to the database before redirecting to the home page.
Update Contact Route:
The /update/<int:id> route allows updating existing contacts. It retrieves the contact by ID, updates its details if the request method is POST, and commits the changes to the database. The form for updating is rendered via the update_contacts.html template.
Delete Contact Route:
The /delete/<int:id> route deletes a contact based on the provided ID and commits the changes to the database, then redirects to the home page.
5. Running the Application:
Finally, app.run(debug=True) starts the Flask development server with debugging enabled, which helps in identifying issues during development.
Conclusion:
This Flask-based backend efficiently handles the core operations of the contact management system—adding, updating, and deleting contacts—while interacting seamlessly with the SQLite database. It serves as the backbone of the application, ensuring smooth and dynamic data handling.




NAME: GABRIEL .I. DIVINE
MATRIC NUMBER: BHU/23/04/05/0112
GITHUB USER NAME: D1V1NEE

INTRODUCTION:
I'm excited to present the update feature of my application. This feature allows users to update contact information efficiently. I'll walk you through the HTML code that powers this feature and explain how each part contributes to its functionality."
The document starts with the doctype declaration, ensuring it's an HTML5 document. We then specify the language as English and set the character encoding to UTF-8. This ensures that the document displays correctly across different browsers and devices."
Head Section
In the <head> section, we include the viewport meta tag to make the page responsive on different screen sizes. The title is set to 'Update Contact, which appears on the browser tab. Additionally, we link to an external CSS file for styling the page, using Flask's url_for function to dynamically generate the URL for the stylesheet:
Body Section
Within the <body> section, we start with a header to indicate the page's purpose clearly.
This makes it immediately clear to the user what this page is for.
Form Element
Next, we have the form element, which is the core
The action attribute specifies the
URL to which the form data will be submitted. This URL is dynamically generated using Flask's url_for function, including the contact's ID to ensure the correct contact is updated.
The method="post" attribute specifies that the form should be submitted using the POST method.
Form Fields
The form contains three fields for the contact's name, phone number, and email address:
Each field is pre-filled with the current contact information using template variables. This ensures the user can see the existing details and make necessary updates.
The required attribute ensures that the form cannot be submitted without these fields being filled out."
Submit Button
The form also includes a submit button that allows the user to submit their changes.
The form also includes a submit button that allows the user to submit their changes.
When this button is clicked, the form data is sent to the specified URL for
processing.
Navigation Link
Finally, we provide a link to navigate back to the home page
This link uses the url for ('home') function to dynamically generate the
URL for the home page, providing a convenient way for users to return to the main page.

NAME: OJO .E. OLUWATOBI
MATRIC NUMBER: BHU/23/04/05/0108
GITHUB USERNAME: EZERELO

Introduction:
Good day everyone. Today, I am going to walk you through how I designed the front end of my app using HTML and CSS.
We'll take a look at some specific CSS rules and how they contribute to the overall design and functionality of the application.
Basic Styling with body and h1
Let's start with the basic styling applied to the body and h1 elements.
The body tag is styled with font-family: Arial, sans-serif;. This sets the default font for the entire app to Arial, with sans-serif as a fallback.
For the h1 tag, text-align: center; is used to center-align the main heading, ensuring that the title is prominently displayed in the middle of the screen.
Links Styling
Next, we have the styling for the a tag, which represents hyperlinks.
text-decoration: none; removes the default underline from links, and color: red; sets the link color to red, making them stand out clearly to the user.
Table Styling
Now, let's look at the table styling. The table tag is styled with width: 100%; and border-collapse: collapse; to ensure the table spans the full width of its container and borders are collapsed into a single border.
Both table and its th and td elements have border: 1px solid #ddd;, creating a light gray border around each cell.
th and td elements are also styled with padding: 8px; and text-align: left;, making the content within each cell neatly aligned and spaced.
th has an additional rule: background-color: #f2f2f2;, which gives the header row a distinct light gray background.
Form Styling
The form element is styled with max-width: 400px; and margin: 0 auto; to center it on the page and limit its width, creating a more user-friendly interface.
label tags are styled with display: block; and margin: 10px 0 5px; to ensure they appear on their own lines with some spacing around them.
input elements are given width: 100%;, padding: 8px;, and margin-bottom: 10px; for full-width input fields with proper spacing and padding.
Banner and Button Styling
The .banner class is used to style a banner section with background-color: #519ff3;, padding: 20px;, and border-radius: 20px;, giving it a distinct background color, rounded corners, and padding for a cleaner look.
Buttons within the app are styled with various classes: .btn, .edit, and .delete. Each button class has a unique background color and padding, as well as border-radius: 20px; for rounded corners. For instance, .btn uses background-color: #afcdee;, while .delete uses background-color: #c90000; to indicate a delete action.
Image Styling
The .imageContact class is used for styling contact images. It sets a fixed size, centers the image, and applies border-radius: 50%; to create a circular image effect.
Interactive Buttons
Lastly, we have the button element styled with background-color: #007BFF;, color: white;, border: none;, and padding: 10px 20px; to create a visually appealing button.
Additionally, cursor: pointer; is added to indicate that the element is clickable. For a hover effect, button:hover changes the background color to a darker shade #0056b3; to give users visual feedback when they hover over the button.
Conclusion
In summary, by using CSS, we can effectively control the layout, appearance, and interactivity of our app, ensuring a better user experience.
Thank you for your attention. I hope this walkthrough has given you a clear understanding of how the front end of my app was designed.


NAME: IHUWE KATER SILAS
MATRIC NUMBER: BHU/23/04/09/0085
GITHUB USERNAME: IHUWE

Introduction
Hello everyone. Today, I'll show you how I designed the home page of my app, Nexa Contacts, using HTML.
 HTML Structure
We start with the basic HTML structure. The <!DOCTYPE html> declaration defines the document type. The <html> tag contains the entire content.
Head Section
"Inside the <head>, we set the character set and viewport for responsive design. The title is 'Contact Management', and we link to an external CSS file for styling.
Body Section
In the <body>, we first have a banner with the app's name, 'Nexa Contacts', inside a <div> and an <h1> tag.
Add New Contact Button
We then have an 'Add New Contact' button, which links to the add_contact route.
Contact Table
Next is the table displaying the contact list. The header section defines the column titles: 'Name', 'Phone', 'Email', and 'Actions'.
 Dynamic Content
In the body section, rows are generated dynamically using Jinja2. Each row displays a contact's details and provides edit and delete links.
Closing Tags
We close the <body> and <html> tags to complete the document.
Conclusion
In summary, this HTML structures the home page of Nexa Contacts, featuring a banner, an add contact button, and a dynamic table for managing contacts. Thank you, and I'm open to questions.


NAME: MUKHTAR YUSUF
MATRIC NUMBER: BHU/23/04/09/0052
GITHUB USERNAME: MUKTYY

Introduction
Hello everyone, today I'll be presenting how I used HTML to design the front end of my application. I'll walk you through the code and explain each part in detail.
HTML Structure
First, let's look at the basic structure of the HTML file. At the very top, we have the <!DOCTYPE html> declaration, which defines the document type and version of HTML we're using.
Head Section
Next, we have the <head> section, which contains meta-information about the document, such as the character set, viewport settings, and the title of the page. The title is displayed in the browser's title bar or tab.
We also link to an external CSS file using the <link> tag, which helps in styling the page.
Body Section
Now, let's move to the <body> section where we have the main content of the page.
We have an image at the top of the page and a heading that says 'Add New Contact'. The class="imageContact" is used to style the image through CSS.
Form Section
Below the heading, we have a form. This form collects the contact details: name, phone, and email. The action attribute specifies the URL to send the form data to, and method="post" indicates that the form data should be sent as a POST request.
Each input field is labeled clearly, and the required attribute ensures that users must fill in these fields before submitting the form.
Navigation
At the bottom of the form, there's a button to submit the form and a link to navigate back to the home page.
The class="btn" is used to style the link as a button through CSS.
Conclusion
In conclusion, this HTML code structures the front end of the 'Add Contact' page, ensuring a clear and user-friendly interface for adding new contacts. The use of external CSS for styling and Flask's url_for for URL handling demonstrates a clean separation of concerns and maintainability.

SCREENSHOT OF GITHUB CONTRIBUTION PAGE FOR THE PROJECT

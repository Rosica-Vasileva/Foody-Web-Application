## foody-web-application-testing-guide

### Overview

Welcome to the Foody Web Application Testing Guide! This guide is designed to help beginner manual QA testers understand the functionalities of the Foody web application and provide a structured approach to testing.

#### Project Description

Foody is a web application that allows users to share their food experiences. The application has various features, including user registration, login, profile management, food creation, and food management.

#### Accessing Foody

You can access the Foody application on the following URL: [Foody Web App](http://softuni-qa-loadbalancer-2137572849.eu-north-1.elb.amazonaws.com:85)

## Test Cases

### Use Case 1: Home Page

**Test Case 1.1: Verify Home Page for Unregistered/Non-Logged Users**
1. Open the Foody application URL.
2. Confirm that the Home page is displayed with a navigation bar, including "Foody Home," "SIGN UP," and "LOG IN" buttons.
3. Scroll through the Home page to ensure sections like "Share your food," "Describe Your Dish," and others are visible.

**Test Case 1.2: Verify Home Page for Logged Users**
1. Log in to the Foody application.
2. Check if the Home page for logged users displays a welcome message with the user's name.
3. Confirm the presence of navigation links like "User's profile," "Home," "ADD FOOD," and "LOGOUT."

### Use Case 2: User Registration

**Test Case 2.1: Verify Successful User Registration**
1. Navigate to the Sign-Up page from the Home page.
2. Fill in valid information in the registration form.
3. Click the "SIGN UP" button.
4. Ensure the user is successfully registered and redirected to the Home page for logged users.

**Test Case 2.2: Verify Terms and Conditions Link**
1. Navigate to the Sign-Up page.
2. Click on the hyperlink to view the Terms and Conditions.
3. Confirm that the document is accessible and readable.

### Use Case 3: User Sign In

**Test Case 3.1: Verify Successful User Login**
1. Navigate to the Login page from the Home page.
2. Enter valid credentials (username and password).
3. Click the "LOG IN" button.
4. Confirm that the user is successfully logged in and redirected to the Home page for logged users.

**Test Case 3.2: Verify Forgot Password Functionality**
1. On the Login page, click on the "Forgot password" option.
2. Follow the steps to restore the password via a verified email.
3. Confirm that the password is successfully restored.

### Use Case 4: Profile Management

**Test Case 4.1: Verify Navigation to My Profile**
1. Log in to the Foody application.
2. Click on the "User's profile" link in the Navbar.
3. Confirm that the user is redirected to their profile page.

**Test Case 4.2: Verify Edit Profile Information**
1. Navigate to the My Profile page.
2. Click the "EDIT" button.
3. Modify profile information, including profile picture, first name, last name, and about me sections.
4. Confirm that the changes are successfully saved.

### Use Case 5: Food Creation

**Test Case 5.1: Verify Navigation to Add Food Page**
1. Log in to the Foody application.
2. Click on the "ADD FOOD" button on the Home page.
3. Confirm that the user is redirected to the Add Food page.

**Test Case 5.2: Verify Successful Food Creation**
1. Navigate to the Add Food page.
2. Fill in valid information for food creation (title, description, and URL).
3. Click the "ADD" button.
4. Confirm that the new food is added, and the user is redirected to the Home page.

### Use Case 6: Food Management

**Test Case 6.1: Verify Presence of Food on Home Page**
1. Log in to the Foody application.
2. Check if the Home page displays the list of created foods for the logged user.

**Test Case 6.2: Verify Options for Each Food (View, Edit, Delete)**
1. On the Home page, find a created food.
2. Confirm the presence of options to view, edit, and delete the food.
3. Perform each action and verify its success.

## Postman Requests

1. **Log in to the API:**
   - Method: POST
   - Endpoint: /api/User/Authentication
   - Request Body: { "userName": "yourUsername", "password": "yourPassword" }

2. **Create a New Food:**
   - Method: POST
   - Endpoint: /api/Food/Create
   - Request Body: { "name": "New Food", "description": "Description of the new food", "url": "http://example.com/image.jpg" }

3. **Search for the Food You Created:**
   - Method: GET
   - Endpoint: /api/Food/Search?keyword=New Food

4. **Change the Title of the Food You Created:**
   - Method: PATCH
   - Endpoint: /api/Food/Edit/foodId
   - Request Body: [{ "path": "/name", "op": "replace", "value": "Updated Food Title"}]

5. **Delete Food:**
   - Method: DELETE
   - Endpoint: /api/Food/Delete/foodId

## How to Submit Your Work

1. Create a .zip archive containing:
   - Test-Management-and-Bug-Tracker.xlsx file.
   - JSON file with your Postman collection.

2. Upload your archive to the SoftUni website in the Regular Exam section.


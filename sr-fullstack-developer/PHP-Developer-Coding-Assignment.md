# PHP Developer Coding Assignment:

Let's consider there is a user registration form

### Below are the form fields
- Name
- Username
- Password
- Confirm Password
- Profile Picture
- Zip Code

### Expected Flow
- When the user clicks on the Submit button, the form will get submitted
- Please note, the Profile Picture field should upload an image using AJAX not on form submit
- Once the profile pic is uploaded, we should be able to see the preview of the uploaded image in the form itself
- We should have a loading screen while uploading an image. Once uploaded the loading screen should be hidden
- Uploaded image should have an option to delete it using AJAX

### Expected PHP Structure - MVC, OOPS
- A class should be used e.g. Class User
- All the form field should be treated as the class variable of the User object
- validate(), this function should validate all the elements of the posted Form and return boolean
- save(), it will save the entry to the user table
- getErrors(); if validation fails then this function should return HTML formatted message for all the error

### Expected JavaScript Structure - Use a single JS file with an Object-Oriented mechanism
- All the JS code should be written in a single file
- Make sure the code is reusable as much as possible (Hint: AJAX calls)

### Expected MySQL Tables
- users
- images

# Assessment Criteria
- Use proper indexing
- Use best practices to ensure XSS, CSRF, SQL injection etc are taken care of

# Deliverable
Create a repository in your github account and commit the code into that repository. Send us the link to the repository.

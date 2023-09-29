# Backend Coding Challenge

[![Build Status](https://github.com/Thermondo/backend-code-challenge/actions/workflows/main.yml/badge.svg?event=push)](https://github.com/Thermondo/backend-code-challenge/actions)

We appreciate you taking the time to participate and submit a coding challenge. In the next step we would like you to
create/extend a backend REST API for a simple note-taking app. Below you will find a list of tasks and limitations
required for completing the challenge.

### Application:

* Users can add, delete and modify their notes
* Users can see a list of all their notes
* Users can filter their notes via tags
* Users must be logged in, in order to view/add/delete/etc. their notes

### The notes are plain text and should contain:

* Title
* Body
* Tags

### Optional Features 🚀

* [ ] Search contents of notes with keywords
* [ ] Notes can be either public or private
    * Public notes can be viewed without authentication, however they cannot be modified
* [ ] User management API to create new users

### Limitations:

* use Python / Django
* test accordingly

### What if I don't finish?

Try to produce something that is at least minimally functional. Part of the exercise is to see what you prioritize first when you have a limited amount of time. For any unfinished tasks, please do add `TODO` comments to your code with a short explanation. You will be given an opportunity later to go into more detail and explain how you would go about finishing those tasks.


## FOLDER STRUCTURE

APP LIST-> 
    Account : This app manages user authentication, registration and logout.
    User    : This manages users. Our User model resides here and extends AbstractBaseUser, PermissionsMixin. With this model, we are also implementing our object manager to
    create new user.
    Notes   : This app encapsulates user notes and tags


BDD (Behavior-driven development)

    This give a high level abstraction of how the system should work. Very high...
    We have been able to define the scope of this project using BDD approach


Test cases (TDD): 

    We are also implementing unit test for each of the apps to ensuch integrity


Repository Design Pattern (RDP):

    We are also implementing RDP with our apps. This helps us to keep away major logic from
    our views/controllers. This also strengths uniformity with in the system.


Response Class:

    A custom class is also created to maintain a standard with in our application.
    This class exist with Utils package.


Frontend: 

    Implement a frontend to consume endpoints from our Django application. The frontend is
    built on Vuejs. Just a simple implementation to consume endpoints.
    This is just for me to test and see implementation. Could be helpful visually

    The frontend can be moved out of the Django application to separate concern without breaking anything.

formatter: npx prettier --write "src/**/*.vue"

run test (For each)

    python manage.py test account.tests
    python manage.py test users.tests
    python manage.py test notes.tests

    OR 

    python manage.py test (for all)

API Docs

    http://{host}/docs/


Object Level permission

    We are using the object level permission to manage access to object (notes)
    
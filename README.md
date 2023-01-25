# Portfolio 3
![image](https://user-images.githubusercontent.com/119969411/214307542-1e8835b4-54f0-4230-a5df-237c79ebc1fb.png)

The __*Portfolio 3*__ is an APP, based on a *Python* terminal (which runs in Code Institutes Mock Terminal on Heroku).
The APP provides an automation of reporting logistics to the "*End User*"... Where data is filled into the Terminal, via an Input field - which in return - updates a *SpreadSheet*, for existing and future logistics for their market sales.
This APP will improve the colaboration between business units in a *company* and at the same time "__refactor__" their sales market - for better controlled and optimized sales.

# Features

The __*"Portfolio 3"*__ APP has:

* A Python Terminal and a *Google Spread sheet (gspread)* controlled via an API, from the Terminal.
* The terminal works as a "Macro" for this *gspred* - where all the Calculation relies on the Python Modeling.
* There is a *timestamp* added to the *gspread* for a new stock calculation - so that the user can easy track their Market, and "if wanted" store old-data.

## Existing Features

![image](https://user-images.githubusercontent.com/119969411/214456782-0fd0fe73-b7cd-4758-94da-408c6a3f84db.png)

- There is an *Input* field in the Terminal, which is open for entry when the APP runs.
- There is also validation of all data that has been entrered within the *Input* field.
  * Validation of gspread Range
  * Validation gspread Len
  * Validation of Int numbers
  * Validation of comma separation (for gspread updates)

## Future Features

![image](https://user-images.githubusercontent.com/119969411/214460108-612e7ebc-aaca-4d7a-8eeb-ebfd3da8c904.png)

The APP will be able to:
* Add timestamps to all worksheets within the gspread.
* The Terminal will have a "clear" Terminal option after each run.
* The Error codes thrown at the end-users, will be overviewed and adjusted accordingly
* The *gspread* will be cleared and stored from old-data, to pass this data to a separate worksheet-history sheet.
  - This can be done with a scheduled job.

# Getting Set-up

<img width="362" alt="image" src="https://user-images.githubusercontent.com/119969411/214460750-5b622955-53e5-487d-967f-e297300ed92e.png">

There needs to be a timestamp and a gspread module for the APP to run and execute commands... there for you need to add these Modules in Gitpod:
* TFor these three imports - to the .py file - as shown In the image above:
   1. Two imports for the Gspread and its API
      - These two Imports needs an installation via the Gitpod Terminal (Terminal command: *pip3 install gspread google-auth* )
   2. One import is for the timestamp module
      - The Import for the Timestamp will work with no installation, though it is a part of Python Modelling.

# Testing

The site has been tested within the timeline and resources given, on different devices and different browsers.
PEP8 check has been done, before deployment.

## Validator Testing

![image](https://user-images.githubusercontent.com/119969411/214463288-99eccfef-a7ad-41b6-981e-947f119684b7.png)

### PEP8
No errors were returned when passing through the Code Institutes PEP8 validator.

## Functional Testing


### Bugs -Solved
![image](https://user-images.githubusercontent.com/119969411/214465371-4048d119-acb6-48cc-9de2-58a6685f7b5d.png)
![image](https://user-images.githubusercontent.com/119969411/214465421-517c75f7-65b8-4ae2-8c34-1c3bbca3494c.png)

There was a "*Typo*" found regarding the "next line function" wich was changed from "/n" to "\n".
  - This peace of code could maybe have been removed, but the overal view looked leaner to thave the input field below the input statement,
  - And this change also provided for some extra characters to be added to the input field -for future features (though the line break avoids width spacing).

### Bugs -Remaining
![image](https://user-images.githubusercontent.com/119969411/214465654-c1fc24db-ae1f-45f2-b0d4-82d54c18e0d3.png)
![image](https://user-images.githubusercontent.com/119969411/214465728-b7a382c0-d335-4ae5-8a66-cf248d31050d.png)

The errors thrown to the end-user when typing other things into the Terminal - except comma separated numbers - are confusing (for a non-programmer).
- These Bugs will be remaining though the message still ends upp with __*invalid data- and please try again!*__ and after that error is thrown, a clare text of what is expected for the user is stated within the Terminal (see IMAGES).
  * Note that the "__*Less than 6 numbers*__" errors are all okay (Readable for end-users) - so there only needs to be a change in the "try" statement for all other validation errors in a future release.
    - An introduction course -together with a 1st and a 2nd line support- would easy handle this "bug"... And for an end-user to type in "*bananas*" in a terminal,    that clarely states how and what numbers to type in there, after an *end user introduction*... Well that is a far more serious Issue than the actual bug itself!
    1. BUG REMAINS, for future release!

# Deployment

The site was deployed via GitHub pages:

The __live__ link can be found here - https://portfolio3.herokuapp.com/

(Link for Code: https://github.com/SvenLoevgren/portfolio-3 ).

# Credits

Code Institute education in general coding of HTML, CSS and Java Script - including advice of where to find free content on the web to style the site, plus tools to use to validate the site.
Extra credit to my mentor given by Code Institute, for making it possible to understand the logic of coding and troubleshooting this site.

## Content
The Site and layout was taken from Code institute "Love Maths" project... and adjusted to fit the "Kids Maths" - adding features as sound, text, Summary etc.
Instructions on how to implement the "Division" button was taken from the Code Institute education material.

## Media
Images from *"Pixabay"*, icons from *"Font awesome"*, Fonts from *"Google fonts"*, Logos from *"Code Institute program"*.
Both the logos of title and heading was taken from the Code institute education material (of the "Love Maths" project).

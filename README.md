# Portfolio 3
![image](https://user-images.githubusercontent.com/119969411/214307542-1e8835b4-54f0-4230-a5df-237c79ebc1fb.png)

The __*Portfolio 3*__ is an APP, based on a *Python* terminal (which runs in Code Institutes Mock Terminal on Heroku).
The APP provides an automation of reporting logistics by the "*End User*"... Where data is filled into the Terminal, via an Input field - which in return - updates a *SpreadSheet*, for existing and future logistics for their company market sales.
This APP will improve the collaboration between business units in a *company* and at the same time "__refactor__" their sales market - for better controlled and optimized sales.

# Features

The __*"Portfolio 3"*__ APP has:

* A Python Terminal and a *Google Spread sheet (gspread)* controlled via an API, from the Terminal.
* The terminal works as a "Macro" for this *gspread* - where all the Calculation relies on the Python Modeling.
* There is a *timestamp* added to the *gspread* for all new stock calculated rows - so that the user can easy track their Market, and "if wanted" store old-data.

## Existing Features

### The Terminal

![image](https://user-images.githubusercontent.com/119969411/214456782-0fd0fe73-b7cd-4758-94da-408c6a3f84db.png)

- There is an *Input* field in the Terminal, which is open for an entry when the APP runs.
  * To update sales figures
- There is also validation of all data that has been entered within the *Input* field.
  * Validation of gspread data Range
  * Validation gspread data Len
  * Validation of Int numbers
  * Validation of comma separation (for gspread updates)

### The gpread

![image](https://user-images.githubusercontent.com/119969411/214460108-612e7ebc-aaca-4d7a-8eeb-ebfd3da8c904.png)

There is a Calculation of all 3 worksheets in this gspread (via python code), to state existing stock, surplus data, sales from end-user input and a print of needed stock for the next sales market.

## Future Features

The APP will be able to:
* Add timestamps to all worksheets within the gspread.
* The Terminal will have a predefined -*"clear" Terminal*- entry, after each run.
* The Error codes thrown to the end-users, will be overviewed, and adjusted accordingly, to make them more “*readable*”.
* The *gspread* will be cleared from old-data, to pass this data to a separate worksheet-history sheet.
  - This can be done with a scheduled job.

# Getting Set-up

<img width="362" alt="image" src="https://user-images.githubusercontent.com/119969411/214460750-5b622955-53e5-487d-967f-e297300ed92e.png">

There needs to be a timestamp and a gspread module for the APP to be able to run and execute commands... there for you need to add these Modules in Gitpod:
* For these three imports in the .py file - as shown In the image above, make sure that:
   1. For Two imports… the *gspread* and its *API*:
      - These two Imports needs an installation via the Gitpod Terminal (Terminal command: *pip3 install gspread google-auth* )
      - Note: Default gspread added below this line, but It needs to be set up in Google drive and Google cloud API to work, together with the cred.json file credentials.
        - https://docs.google.com/spreadsheets/d/1OPUMRFogoomR358iH9mxmdqe6XuXhQ_8nCONxVfFuRQ/edit?usp=sharing
   2. One import (See image above) is for the timestamp module
      - The Import for the Timestamp will work with no installation in Gitpod, though it is a part of Python Modelling (and stating IMPORT of this module in the .py file is enough).

# Testing

The site has been tested within the timeline and resources given, on different devices and different browsers.
PEP8 check has been done, before deployment.

## Validator Testing

![image](https://user-images.githubusercontent.com/119969411/214463288-99eccfef-a7ad-41b6-981e-947f119684b7.png)

### PEP8
No errors were returned when passing through the Code Institutes PEP8 validator.

## Functional Testing

### Bugs -Solved
<img width="398" alt="image" src="https://user-images.githubusercontent.com/119969411/214471484-ed422a8b-d8f5-4bc7-a816-369c8531466c.png">
<img width="349" alt="image" src="https://user-images.githubusercontent.com/119969411/214472252-a16930ac-fe94-406d-b7d5-17ac82e55d56.png">

There was a "*Typo*" found regarding the "next line function" which was changed from "/n" to "\n".
  - This peace of code could probably just have been deleted, but the overall view looked leaner to when the end-user input field appeared below the input statement, and this change also provided for some extra characters to be added to the input field -for future features (though the line break now allows more width for the input – without the need to adjust the screen width in the GUI).

### Bugs -Remaining
<img width="668" alt="image" src="https://user-images.githubusercontent.com/119969411/214472804-c90f1ef6-a38d-4ce5-879e-c474bc59cbfb.png">
<img width="673" alt="image" src="https://user-images.githubusercontent.com/119969411/214472916-e813c854-a51a-43d5-b6a0-33ef5ad61cc8.png">

The errors printed to the end-user when typing other things into the Terminal - except comma separated numbers - are confusing (for a non-programmer).
- These Bugs will be remaining though the message still ends up with __*invalid data- please try again!*__ and after that error is thrown, a clear text of what is expected of the users input is printed within the Terminal (see IMAGES).
  * Note that the "__*Less than 6 numbers*__" errors are all okay (Readable for end-users) - so there is only a need for changes in the "try" statement for all other validation errors, __within a future release__.
  * An introduction course -together with a 1st and a 2nd line support- would easy handle this "bug"!... also… for an end-user to type in "*bananas*" in a terminal, that clearly states how to and what numbers to type in there, after an *end user introduction*...well… that’s a far more serious Issue than the actual bug itself!
    - *BUG REMAINS for future a release! *

# Deployment

## Steps
1. Ignore file - checked for the CREDS to not be pushed to Github.
  - This was done via the Gitpod terminal command ( pip freeze > requirements.txt ).
2. Repository pushed to Github.
3. Heroku CREDS and PORT keys updated with needed values.
4. Build Packs added to Heroku
   1. python
   2. node.js
5. Link Heroku APP with Github repository
6. Deploy In Heroku (A manually deploy to main was used)

## Links
The site was deployed via GitHub pages:
The __live__ link can be found here - https://portfolio3.herokuapp.com/
(Link for Code: https://github.com/SvenLoevgren/portfolio-3 ).

# Credits

Code Institute education in general coding with python- including advice of where to find free content on the web to style the APP, plus tools to use to validate the code, plus code content and how to work with external objects with python via API.
Extra credit to my mentor given by Code Institute, for making it possible to understand the logic of coding and troubleshooting this APP.

## Content
The Site and layout was taken from Code institute "Love Sandwiches" project... I then adjusted it all to fit the "Protfolio 3" project/APP- with adding features as styling external gspread and adding timestamps etc.
Instructions on how to implement the *"dictionary, to be displayed at the end of the code running in the APP - for the end users next market advice"*, was taken from the Code Institute education material.

## Media
Initial Spreadsheet from Code Institute "Love Sandwiches project"
Google Drive and API used for connecting to the Spreadsheet.
Heroku Used for APP release.
Over all -  The whole project was built and released with the assistance of Code Institute and based on their "Love Sandwiches" project.


# **Pitts-Technical-Challenge**

# How to use Club Match

Technical Challenge by Timothy Pitts | October 2022 
***
Have you ever wanted to join a club, but just didn't know which one to join! Well, look no farther! With over 500 clubs on campus, it can be difficult to find one that you are interested in joining. Club Match comes with a solution. Simply enter your credentials and select a few of your favorite classes that you have taken, and Club Match will recomend 20 different clubs that have a high compatibility match to your past interests! These instructions will help you to set up the program, and teach you how to use it.


## Requirements
- Below is the list of needed programs and information needed prior to running the program.
- If you are testing outside the OIT Department, Please ask your testing administrator for an AWS Login and a bearer token, and skip to step **2) Installation**

### APIs

* Subscribe to the following BYU APIs:
    * [Persons - v3](https://api-sandbox.byu.edu/store/apis/info?name=Persons&version=v3&provider=BYU/johnrb2&)
    * [Clubs - v1](https://api-sandbox.byu.edu:443/domains/byusa/clubs/v1/clubs)
    * [Students -v3](https://api-sandbox.byu.edu/byuapi/students/v3/${byuID}/enrolled_classes)
    * [Learning Outcomes - v1](https://api-sandbox.byu.edu:443/domains/legacy/learningoutcomes/courseoutcomes/v1/course/{couseNumber})
* If you are testing outside the OIT department, these are already subscribed to and you may move on.
    
### Other APIs

*This API is used, but you don't need to subscribe to it.
    * [Webit Text Analytics](https://webit-text-analytics.p.rapidapi.com/similarity)

#### Instructions for Download and Installaton

### 1) Amazon Web Service
If using for testing purposes, the administrator showing the test functionality will already have their AWS credentials logged in, and you may skip to the next section, and instead refer to the .txt file containing this data.

Log on to [AWS services](https://byulogin.awsapps.com/start#/) and navigate to the BYU AWS Store

![AWS](https://user-images.githubusercontent.com/112526259/198143730-a0a14707-17b7-4698-85f2-0606cc5e5036.PNG)

Under PowerUser, select Command line or programmatic access, then select PowerShell at the top.

(If using Mac or Linux, use those tabs instead. For windows use the powershell terminal for best results)

Copy Option 1

![image](https://user-images.githubusercontent.com/112526259/198144273-f73cc451-9e9a-4724-a685-9880d36b59cb.png)


Paste your [AWS](https://byulogin.awsapps.com/start#/) Credentials into the command line of your CLI
Move on to step 2) Installation

### 2) Installation
1) Clone this repository
   - Open the command terminal
   - Navigate to the file using these commands:
      1) **git clone https://github.com/byu-oit-training/Pitts-Technical-Challenge.git**
      2) **cd Pitts-technical-challenge**
2) Install necessary packages:
   - type into the terminal **npm install**
3) Enter AWS Credentials into terminal
   - See above for how to get AWS Credentials
4) Navigate to the folder in your file explorer containing your project and unzip the db file.
5) Open the Docker Desktop program on your computer
6) Wait 5-10 seconds, or until docker says its running.
7) Type **Docker-compose up -d** into the terminal
8) Wait 5-10 seconds, or until both databases say they are running.
9) Execute program:
   - type in to the terminal **node main.js**
10) Move on to Usage below

### How it works:
Club Match uses a semantic comparison API, and uses AI to intelligently compare the classes you have previously taken with Clubs offered on BYU campus. It will allow you to find, save, and view different clubs that you may have interst in. Then, it will allow you to delete any clubs data, or all data from your profile if you would like.

## Usage:
1. Open the program, and enter node main.js into the command line.

![Start](https://user-images.githubusercontent.com/112526259/199831049-a177f70b-7696-4089-9f72-d11eeff42fd3.PNG)

2. Enter Your BYU ID when prompted to.
3. Enter Your Bearer Token

![Menu](https://user-images.githubusercontent.com/112526259/199831742-4b393de3-1862-41b1-881b-3c72df10a3a9.PNG)

4. Select any of the menu options, then find the section below for the option selected.

#### Select "Find a Club"
   - After the menu is done loading, select any number of past classes that you enjoyed.
   - The program will compare your classes to the avaliable list of campus clubs
   - After it finished, select any number of clubs you are interested in to save to the internal database.
#### Select "View Saved Clubs"
   - Upon selecting, scroll up or down to see all the past clubs you have saved.
#### Select "Delete all saved clubs"
   - Upon selecting you will be asked to confirm, enter **Y** for yes, or **N** for no.
#### Select "Delete one saved club"
   - Select one club that you would like to remove from your saved list.
   - When asked, enter **Y** to confirm or **N** to return to the main menu.
#### Exit
   - Exits the program.

### After using the program
   - Please fill out this link to help test the program.
   - https://forms.gle/VUkxAd4qJG9KVo7WA

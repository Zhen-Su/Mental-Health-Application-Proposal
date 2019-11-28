# Requirements Analysis

## Functional Requirements

#### 1. Cloud-based

<!--The local system must be able to
- Upload local user data to server to have information stored in cloud
- Upload data to server whenever local data is modified, if server unreachable: re-attempt upload when connection restored
- Fetch data from server in case of logging in -->

- The local app will ensure the user will be able to retrieve their accounts and the contents from the cloud database onto a new device.
    - The app must upload user data to server to sync user account information accross the number of devices the user is using.
    - The app will upload user data to server within set time period
        - The app will upload new changes in the users **Bham** calendar if given account credentials. (see: 6. Account Mangement)
        - The app will upload new changes in the users **Canvas** calendar if given account credentials. (see: 6. Account Mangement)
        - The app will upload user-input personal information.
        - the app will upload user-collected information.
        - The app will upload up-to-date caldendar configuration.
    - The app will fetch user data from server within set time period
    - The app will resolve changes between devices to prevent conflicts in information


    - In case of unreachable to cloud server, will attempt upload once re-established connection.
    

***Non-functional***
- Send and retrieve data securely
- Try to reduce downtime of server (implement in a way that performance-heavy tasks are executed by local application if possible)
- Data sync should not significantly impact system performance

#### 2. Registration and Login

- The user will not be able to access the main functionalities of the app until they have either logged in or signed up for an account to log in.
    - The app will check if there is an account registered and log in, otherwise, the user will be directed to a log-in screen and has the option to create an account.
        - The user will log in with their credentials, email and password.
        - Once logged in, the user can choose to save credientials for automatic login next time they start the app.
        - For security reaons, user credentials are stored in the cloud (see: 1. Cloud-based) as well as locally. 
        - New password resets will be uploaded to the cloud, which is compared against locally saved password. 
        - Unchanged local password will fail once compared to new credentials recorded in cloud server.


    - When signing up for an account, the app will direct them to a new screen.
        - The user must provide the app with their credentials as email and password, of which a confirmation email will be sent to their account to affirm existance of email account.
        - The user can provide the app with their Bham credentials, of which they will be asked to login to confirm credentials. 
            - The app will extract the information regarding schedule from their Bham account, and insert it into the calendar (see: 3. Calendar)
        - The user can provide the app with their Canvas credentials,of which they will be asked to login to confirm credentials.
            - The app will extract information regarding deadlines and add to the calendar and todo(see: 3. Calendar, 4.Todo) 
        - The user can provide their personal information through the questionaire as part of the sign-up process. The user can choose to answer any number of the questions as to not turn the user away from the app through too much input given. 
            - However, it is encouraged that the user provide the app which as much information as they are willing to. 
            - Because this allow the app to personallize the main components (see: 3. Calendar, 4. Todo) through its AI (see: 7. AI).
        - The user will be able to add or remove personal information in their account management after signup (see: 6. Account Management)  

    - If the user has an account but forgot the password, they can opt to reset password by sending it to the email they used to register their account with.


<!--
The user is able to
- Create an account
- Login using credentials (email and password)
- Reset password
- Save login/Remember password

The system can
- Store user data locally (and upload to the cloud (see: Cloud-based))

Login process:
1. User interface for login
    - fields: email, password
    - box: save password
    - links: forgot password, register
    - login button
    - wrong password or email popup if information entered is wrong
2. If login from new device, send verification email/text.
3. Main Page

Registration process:
1. User interface for registration
   - fields: name, email, password, confirm password
   - info: password requirements, notice of clicking on Sign up button
   - hyperlink: T&C and PP
   - button: Sign up, Back button (to login page)
2. User interface to confirm email
   - back button
3. Link mobile phone to account (optional)
   - enter phone number and then enter code sent via text message
   - or skip
4. Questionnaire (to be defined), used to gather information on how systems will work / be able to help user
5. Main Page (to be defined which page is default page) --->

***Non-functional***
- Password verification
- use cookies / ip to determine if login is from a new device.
- Email confirmation (and email verification)
- Phone verification message should be sent in small time frame.
- Store user data securely

#### 3. Calendar

- The user will be able to modify the calendar upon signing into their account.
    - The user can add an event given information on name, date and length, with length 0 being a deadline event.
    - The user can provide additional information on the event
        - location of event
        - the pattern of the event of if it is a recurring event.
    - The user can delete an event, duplicate the event, or edit any sub-information belonging to the event.
        - the user will be able to specify if they are modifying for all subsequent events of the same name, or just the instance of the choosen event.
- The app will to modify the calendar by fetching calendar information from Bham and Canvas calendar, if given access by user.
    - The app will have access to modification rights as if it was another user.
    - The app will not consult user on adding events taken from the external sources, but the user is able to treat them as an user-added event.
- The app will attempt to modify the caldendar based on user-collected information from both the tracker (see: 5. Tracker), and personal information given from questionaire (see: 6. Account Management), using AI (see: 7. AI).
    - The calendar will receive recommended output from AI based on given information to schedule the calendar with daily tasks.
    - The user can choose to accept none to all of the recommendation the AI makes, to commit to their weekly schedule.
    - The AI will manage 2 weeks worth of recommendation of daily task, to account for changes in actual schedule which leads to uncertainty.


<!--
User can
- Add an event
- Add groupings (color code for events)

System can
- Fetch lecture dates from my.bham into grouping and events
- Fetch deadlines from Canvas into grouping and events
- Displays calendar in some format (to be determined)
-->

#### 4. ToDo
- The todo acts as a daily representation of the calendar, and thus syncs information between itself and the Calendar. 
- It will display it in a phone-friendly format to allow user to better see task requirements for the day, in a focused manner. 
    - It will add User events, Calendar events, and AI events and display them for user based on current date.
- The user can create/edit/delete a todo in the same manner as they can an event in a calendar (see: 3.Calendar)
    - The new todo changes will be synced to calendar as an event.


<!--
User can
- add todo
    - name todo
    - add notes
    - color code
    - add category
- edit todo
    - edit categories above
- remove todo

- The user can add todo
- The system can extract Canvas events as todo deadlines-->

#### 5. Tracker


First time
- Request permission to access existing tracked information on device (e.g. Health apps)

System can
- import tracking data from all permitted tracking applications
- display progress for different time intervals (day, week, month, year)
- perform tracking analysis to recommend user options of improvement (see: Tracker process)
- send reward notification when achieving goals

User can
- Add tracking data manually (e.g. [+] slept x hours)
- Remove manually entered tracking data

Tracker process:
1. Create recommendation based on tracking AI (trained to recommend based on positive changes of the user?)
2. Send notification to user (e.g. slept sufficiently / caught up on sleep tonight)

***Non-functional***
- Perform tracking analysis every hour
- Appealing interface for progress of tracking so user is more likely to add tracking information

Extendable:
- Import data from more third party apps people might be already using
- Compare to friends (if option is turned on) and add tokens (achievements)

#### 6. Account Management
Change account login details (email/password)
1. Enter current and new email/password.
2. UI to change credentials
   - fields: old password, new password, confirm new password
   - confirm and cancel box

Add Phone
1. Enter phone number
2. Verification code sent via sms
3. Enter verification code.

Show devices
- Show the user all the devices that are logged into the account
- allow user to log out any of these devices so these devices must re-enter login details and get kicked out of current session


***Non-functional***
- check if password is of a certain complexity
  - \> 10 signs total, < ? signs total
  - must contain at least one of each: LC letter, UC letter, symbol, digit
- sending verification email/ messages should be done in small time frame
- store all new user data securely


#### 7. AI

- The AI will create scheduling models based on collected information from other functionalities of the app that the user can access
    - The AI collects information based on changes from the Calendar (see: 3. Caldendar), User-given personal information (see: 6. Account Management), and from Tracker (see: 5. Tracker)
    - The AI will attempt to sort the information coming in to produce an optimized schedule for a period of 2 weeks.
    - The AI will recommend modification to it own schedule model for the week based on actual user activity throughout the day.
        - i.e recommends more sleep hours next day if User report light sleep previous day.
    - The AI will change its recommendation models based on how much of the models it recommend the user is rejected or accepted to study user preferences.

- The AI must be able to be switched on or off by user, as well as its saved profile on user preferences be deletable. 

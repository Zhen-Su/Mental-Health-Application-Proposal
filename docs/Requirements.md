# Requirements

## Cloud-based

The local system must be able to
- Upload local user data to server to have information stored in cloud
- Upload data to server whenever local data is modified, if server unreachable: re-attempt upload when connection restored
- Fetch data from server in case of logging in

***Non-functional***
- Send and retrieve data securely
- Try to reduce downtime of server (implement in a way that performance-heavy tasks are executed by local application if possible)
- Data sync should not significantly impact system performance

## Registration/Login

The user is able to
- Create an account
- Login using credentials (email and password)
- Logout
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
5. Main Page (to be defined which page is default page)

***Non-functional***
- Password verification
- use cookies / ip to determine if login is from a new device.
- Email confirmation (and email verification)
- Phone verification message should be sent in small time frame.
- Store user data securely

## Calendar

User can
- Add an event
- Add groupings (color code for events)

System can
- Fetch lecture dates from my.bham into grouping and events
- Fetch deadlines from Canvas into grouping and events
- Displays calendar in some format (to be determined)

### ToDo

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
- The system can extract Canvas events as todo deadlines

## Wiki

contains
- useful information for the student's mental health (also links to existing services and assistance at uni)
- useful information and tips on any tracking-related topics

## Tracker

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

## Account Management
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

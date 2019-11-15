# Requirements

## Cloud-based

- Update server with local data from user to have information stored in cloud
- Data sync whenever local data is modified, if server unreachable: re-try syncing when connection restored
- Fetch data from server in case of logging in from a new device

***Non-functional***
- Save and retrieve data securely
- Try to reduce downtime of server
- Data sync should not significantly impact system performance

## Registration/Login

- Create an account
- Login using credentials (email and password)
- Reset password
- Save login/Remember password
- Logout
- Store user data in cloud

Login process
1. User interface for login (fields: email, password, save password; links: forgot password, register, login button)
2. If login from new device, send verification email/text.
3. Main Page

Registration process:
1. User interface for registration
   - fields: name, email, password, confirm password
   - info: password requirements
   - box tick: accept T&C and PP
   - link: register
2. User interface to confirm email
   - back button
3. Link mobile phone to account (optional)
   - enter phone number and then enter code sent via text message
   - or skip
4. Questionnaire (to be defined), used to gather information on how systems will work/help user
5. Main Page

***Non-functional***
- Password verification
- use cookies/ ip to determine if login is from a new device.
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

## ToDo

- The user can add todo
- The system can extract Canvas events as todo deadlines

## Wiki

- The wiki has pages containing useful information for the student's mental health

## Tracker

First time
- Request permissions of accessing existing tracked information on device (e.g. Health apps)

System can
- display progress
- extract data automatically from existing trackers (optional)
- perform tracking analysis (to recommend user options of improvement)
- send reward notification when achieving goals (opt. add tokens)

User can
- Add tracking information manually (e.g. [+] slept x hours)

Tracker process:
1. Create recommendations based on tracking AI Big data analysis
2. Send notification to user (e.g. slept sufficiently / caught up on sleep tonight)

***Non-functional***
- Perform tracking analysis every hour
- Appealing interface for progress of tracking

Extendable:
- Track from more apps
- Compare to friends?

## Account Management
Change account login details (email/password)
1. Enter current and new email/password.
2. UI to change credidentials
- fields: old password, new password, retype new password
- confirm and cancle box

Add Phone
1. Enter phone number
2. Verification code sent via sms
3. Enter verification code.

Show devices
- Show the user all the devices there account is logged into
- allow user to logout of any of the devices. requre verificaton upon loging back into that device.

***Non-functional***
- check password is of a certain complexity
- sending verification email/ messages should be done in small time frame
- store all new user data securely

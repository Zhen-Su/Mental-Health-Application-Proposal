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
- Save login/Remember password
- Logout
- Store user data in cloud

Login process
1. User interface for login (fields: email, password, save password; links: forgot password, register, login button)
2. Main Page

Registration process:
1. User interface for registration
   - fields: name, email, password, confirm password
   - info: password requirements
   - box tick: accept T&C and PP
   - link: register
2. User interface to confirm email
   - back button
3. Questionnaire (to be defined), used to gather information on how systems will work/help user
4. Main Page

***Non-functional***
- Password verification
- Email confirmation (and email verification)
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

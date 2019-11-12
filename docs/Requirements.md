# Requirements

## Functional Requirements

### Cloud-based

- Update server with local data from user to have information stored in cloud
- Download from server to fetch current status of data in case of using different device

Non-functional requirements:

- Do so securely
- Try to reduce downtime of server
- data sync should not significantly impact system performance
- data sync whenever local data is modified, if server unreachable: re-try syncing when connection restored


### Registration/Login

Be able to
- Create an account
- Login using credentials (email and password)
- save login
- Logout

- First login with new device: Fetch data from server

- Store user data

Login process:
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


Non-functional requirements:

- Password verification
- Email confirmation (and email verification)
- Store user data securely


### Calendar

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

System can
- Extract Canvas events as todo deadlines

### Wiki

Kinda obvious

### Tracker

First time:
- Request permissions of accessing existing tracked information on device (e.g. Health apps)

System can
- display progess
- extract data automatically from existing trackers (optional)
- perform tracking analysis (to recommend user options of improvement)
- send reward notification when achieving goals (opt. add tokens)

User can
- add tracking information manually (e.g. [+] slept x hours)

Tracker process:
1. create recommendations based on tracking AI Big data analysis
2. send notification to user (e.g. slept sufficiently / caught up on sleep tonight)

Non-functional requirements:

- perform tracking analysis every hour
- Appealing interface for progress of tracking

extendable: 
- track from more apps
- compare to friends?
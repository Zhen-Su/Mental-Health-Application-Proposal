# Requirements

## Functional Requirements

### Cloud-based

- Update server with local data from user:
- data upload

#### Non-functional 

- Do so securely
- Try to reduce downtime of server
- data sync should not significantly impact system performance
- data sync whenever local data is modified, if server unreachable: re-try syncing when connection restored


### Registration

- Create an account
- Login using credentials (email and password)
- First login with new device: Fetch data from server
- save login
- Logout

- Store user data

Login process:
- User interface for login (email, password, save password, forgot password, register, login)
- Main Page

Registration process:
- User interface for registration  (name, email, password, confirm password, password requirements, accept T&C and PP, register)
- User interface to confirm email (back button)
- Questionnaire (to be  defined)
- Main Page

#### Non-functional registration

- Password verification
- Email confirmation (and email verification)
- Store user data securely


### Calendar

- Add an event
- Add groupings (color code for events)

- Extracts lecture dates from my.bham into grouping and events
- Extracts deadlines from Canvas into grouping and events

- Displays calendar in a format

### ToDo

- add todo

- Extract Canvas events as todo deadlines

### Wiki

### Tracker

First time:
- Request permissions of tracking information on device

- display progess
- add tracking information manually
- extract automatically from existing trackers (optional)
- tracking analysis every hour
- reward notification when achieving goals (opt. add tokens)

Tracker process:
1. create recommendations based on tracking AI Big data analysis
2. sends notification to user

#### Non-functional

- Appealing interface for progress

extendable: 
- track from more apps
- compare to friends
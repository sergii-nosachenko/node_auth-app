# Auth endpoint
This application allows user to:
- Register using name, email and password (only non authenticated)
  - Inform the users about the rules for a password and check them
  - send and activation email
- Actvation page (only non authenticated)
  - the user should be activated only after email confirmation
  - redirect to Profile after the activation
- Login with valid credentials (email and password) (only non authenticated)
  - If user is not active ask them to activate their email
  - Redirect to profile after login
- Logout (only authenticated)
  - Redirect to login after logging out
- Password reset (only non authenticated)
  - Ask for an email
  - Show email sent page
  - add Reset Password confirmation page (with `password` and `confirmation` fields that must be equal)
  - Show Success page with a link to login
- Profile page (only authenticated)
  - You can change a name
  - It allows to change a password (require an old one, `new password` and `confirmation`)
  - To change an email you should type the password, confirm the new email and notify the old email about the change
- 404 for all the other pages

# Expenses endpoint

- An expense have a
  - user
  - date
  - title
  - amount
  - category (just a label for now)
  - note (optional text)
- Expenses are stored in a Postgres DB
- You have ability to get the stats for (with query params)
  - some period (from - to)
  - some user
  - some categories (one or several)

  Client code is [here](https://github.com/sergii-nosachenko/react_accounting-app-with-db-and-auth/tree/develop)

  [WORKING DEMO](https://sergii-nosachenko.github.io/react_accounting-app-with-db-and-auth/)

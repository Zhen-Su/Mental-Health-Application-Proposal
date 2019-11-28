# Important notes

These notes are a collection of considerations that need to be added to our documentations as they are crucial to our application.

## Security

- We do not specify how our secure data transfer connection works. We should use **hybrid cryptography** which involves a number of steps between server and local application (refer to [this page](https://medium.com/mindorks/how-to-pass-large-data-between-server-and-client-android-securely-345fed551651))
- Additionally local data of the app should probably be encrypted as this is common practice for sensitive data. (refer to [this page](https://security.stackexchange.com/questions/145742/why-encrypt-sensitive-mobile-app-data)). This is presumably especially true for a _remember password_ function as it stores email and password locally.

# Android Event Tracking App: EventTracker

**Mobile app created for CS 360: Mobile Architecture and Programming**

  EventTracker is an Android app I developed to help users keep track of appointments and upcoming events without a complicated interface or needing several different tools. The project combines user-centered design with Java, SQLite, and optional SMS reminders.

## 1. Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?

  The goal of EventTracker was to make everyday scheduling and event tracking easier and more organized. Users needed a way to create an account, log in, and add, view, edit, or delete events with a name, date, time, and optional details. The app also needed to keep event information saved between sessions and offer optional reminders. I wanted the basic event-tracking features to remain useful even if the user declined permission to send SMS messages.

## 2. What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?

  The app includes account creation and login, an event display, forms for adding and editing events, and settings for optional SMS reminders. I focused on straightforward navigation and clear event information so users could quickly check their plans or make changes without having to learn a complicated system. Keeping the design simple and making reminders optional helped support different user preferences while keeping the main purpose of the app clear.

## 3. How did you approach the process of coding your app? What techniques or strategies did you use? How could those techniques or strategies be applied in the future?

  I started with the interface designed for Project Two and then worked on connecting the screens to actual functionality in Android Studio. Rather than trying to code everything at once, I worked through the login system, SQLite database operations, and SMS permission and reminder features in stages. The database stores user accounts and event information, while separate settings store the user's SMS preferences. Building and testing features a little at a time helped make troubleshooting more manageable, and it is an approach I plan to use in future projects. I also utilized debugging tools like Logcat to pinpoint where problems were originating, which helped tremendously.

## 4. How did you test to ensure your code was functional? Why is this process important, and what did it reveal?

  I used the Android Emulator to test the main app functions and check how the app responded to user actions. This included working through account access, adding and changing event information, and the optional SMS permission behavior. An important requirement was that users could still use the event-tracking features if they denied SMS permission. The reminder worker ran in the emulator, although I did not confirm delivery of an actual text message. Testing throughout development helped me catch issues earlier and reminded me that code compiling successfully does not necessarily mean every feature works as intended.

## 5. Consider the full app design and development process from initial planning to finalization. Where did you have to innovate to overcome a challenge?

  One challenge was adding the required SMS reminder feature without making it necessary for the rest of the application. I had to think about permissions, user choices, and what should happen when permission was denied. Keeping reminder functionality separate from the core event features was an important design decision. If I prepared the app for a public release, I would also consider replacing direct SMS with device notifications, since Google Play has restrictions on SMS permissions and local notifications would fit this type of app better.

  I also encountered an issue where a saved phone number was being used for all users instead of just the signed-in user. I went back and fixed this so that each user, even on a shared device, could choose whether to opt in or out of reminders. Another issue was related to security. The password field would remain populated on the login screen even after navigating away. I changed this so the password field would clear when leaving the screen, preventing someone else from simply pressing the login button to access the account.

## 6. In what specific component of your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?

  I am particularly proud of connecting the event interface to the SQLite database so users can create, view, update, and delete event information. This project helped me move beyond designing what an app should look like and understand more about the code and data handling needed to make it functional. I also gained experience thinking about security, including storing passwords as salted hashes rather than plain text and requesting only permissions the app needs.

## Project Status

  This is a course portfolio project and has not been published as a Google Play app. SMS scheduling and permission handling were implemented for the assignment, but real SMS delivery was not confirmed. Additional testing and review would be needed before a public launch. I may continue improving the app with the goal of eventually publishing it.

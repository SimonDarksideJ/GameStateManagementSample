# Game State Management Sample
MonoGame version of the GameStateManagement Sample

Game State Management (Mango, C#/VB)
Area
Games: Gameplay, User Experience
Submitted
15/03/2017
Code Sample

Description:

This sample shows how to manage the transitions among menus and gameplay states.

Sample Overview

This sample provides a simple game screen management system, ready to be used as a starting point for games with MonoGame. Additionally the sample includes example games for all MonoGame platforms including Android, iOS, Windows, Linux. Showing how you can build different, targeted experiences for each platform while using the same base code. Each experience is different to emphasize the versatility of the core library to create different experiences.

The ScreenManager class is a reusable component that maintains a stack of one or more GameScreen instances. It coordinates the transitions from one screen to another, and takes care of routing user input to whichever screen is on top of the stack.

Each screen class (including the actual gameplay, which is just another screen) derives from GameScreen. This provides Update, HandleInput, and Draw methods, plus some logic for managing the transition state. GameScreen doesn't actually implement any transition rendering effects, however: it merely provides information such as "you are currently 30% of the way through transitioning off," leaving it up to the derived screen classes to do something sensible with that information in their drawing code. This makes it easy for screens to implement different visual effects on top of the same underlying transition infrastructure.

The sample also includes functionality for handling tombstoning and fast app switching on Windows Mobile. The ScreenManager works with an IScreenFactory to store away a list of the current screens and bring them back when the game resumes. Each GameScreen has methods for Activate and Deactivate that can be used to retrieve and store additional state about the game so you can bring the user back exactly where they were.
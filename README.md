# Game State Management (Mango, C#/VB)

|Area|Submitted|Type|
|-|-|-|
Games: Gameplay, User Experience|5/24/2011|Code Sample
||||

## Description

This sample shows how to manage the transitions among menus and gameplay states.

## Sample Overview

This sample provides a simple game screen management system, ready to be used as a starting point for games on Windows Phone, Xbox 360, or Windows. Additionally the sample includes example games for Windows Phone as well as Windows/Xbox 360, showing how you can build different, targeted experiences for each platform while using the same base code. Each experience is different to emphasize the versatility of the core library to create different experiences.

The ScreenManager class is a reusable component that maintains a stack of one or more GameScreen instances. It coordinates the transitions from one screen to another, and takes care of routing user input to whichever screen is on top of the stack.

Each screen class (including the actual gameplay, which is just another screen) derives from GameScreen. This provides Update, HandleInput, and Draw methods, plus some logic for managing the transition state. GameScreen doesn't actually implement any transition rendering effects, however: it merely provides information such as "you are currently 30% of the way through transitioning off," leaving it up to the derived screen classes to do something sensible with that information in their drawing code. This makes it easy for screens to implement different visual effects on top of the same underlying transition infrastructure.

The sample also includes functionality for handling tombstoning and fast app switching on Windows Phone. The ScreenManager works with an IScreenFactory to store away a list of the current screens and bring them back when the game resumes. Each GameScreen has methods for Activate and Deactivate that can be used to retrieve and store additional state about the game so you can bring the user back exactly where they were.

> All content and source code downloaded from this page are bound to the Microsoft Permissive License (Ms-PL).

Download | Size | Description
---|---|---|
[GSMSample_4_0_Mango](https://github.com/simondarksidej/XNAGameStudio/tree/archive/Samples/GSMSample_4_0_Mango) | 0.16MB | Source code and assets for the Game State Management Sample (XNA Game Studio 4.0 Refresh - Mango).
[GSMSample_4_0_Mango.zip](https://github.com/simondarksidej/XNAGameStudioZips/raw/zips/GSMSample_4_0_Mango.zip) | 0.16MB | Source code and assets for the Game State Management Sample (XNA Game Studio 4.0 Refresh - Mango).
[GSMSample_4_0_Mango_VB](https://github.com/simondarksidej/XNAGameStudio/tree/archive/Samples/GSMSample_4_0_Mango_VB) | 0.16MB | Source code and assets for the Visual Basic version of the Game State Management Sample (XNA Game Studio 4.0 Refresh - Mango).
[GSMSample_4_0_Mango_VB.zip](https://github.com/simondarksidej/XNAGameStudioZips/raw/zips/GSMSample_4_0_Mango_VB.zip) | 0.16MB | Source code and assets for the Visual Basic version of the Game State Management Sample (XNA Game Studio 4.0 Refresh - Mango).
[GSMSample_4_0_PHONE](https://github.com/simondarksidej/XNAGameStudio/tree/archive/Samples/GSMSample_4_0_PHONE) | 0.12MB | Source code and assets for the Windows Phone version of the Game State Management Sample (XNA Game Studio 4.0).
[GSMSample_4_0_PHONE.zip](https://github.com/simondarksidej/XNAGameStudioZips/raw/zips/GSMSample_4_0_PHONE.zip) | 0.12MB | Source code and assets for the Windows Phone version of the Game State Management Sample (XNA Game Studio 4.0).
[GSMSample_4_0_WIN_XBOX](https://github.com/simondarksidej/XNAGameStudio/tree/archive/Samples/GSMSample_4_0_WIN_XBOX) | 0.15MB | Source code and assets for the Windows/Xbox 360 version of the Game State Management Sample (XNA Game Studio 4.0).
[GSMSample_4_0_WIN_XBOX.zip](https://github.com/simondarksidej/XNAGameStudioZips/raw/zips/GSMSample_4_0_WIN_XBOX.zip) | 0.15MB | Source code and assets for the Windows/Xbox 360 version of the Game State Management Sample (XNA Game Studio 4.0).
||||

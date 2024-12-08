The basic project setup for each app is same. I am using Android Studio to construct the sample. 

programs in this book, but you may use another editor, such as IntelliJ or Visual Studio Code. 

The method in Android Studio is as follows: you start a new Flutter project. 

Choose the Flutter application as the project type (template) and input a project name. The 

The Flutter software development kit (SDK) then generates the project for you, including generating 

The project directory has the same name as the project itself. In the project directory, the library 

The folder includes the main.dart file containing the source code (in other words, project_name/lib). 

main.dart). You'll also have an android folder for the Android app, and an iOS folder. 

Start Android Studio. 

The folder name ch2_my_counter, which is the same as the project name, is used to generate a Flutter project. It shows how to update a counter by hitting the + button and makes use of the default Flutter project template. The Material Design elements of Android are used by default. Flutter projects frequently use motion, visual, and behavioural widgets. The main.dart file is the first thing that runs when the program is launched, and each project has its own directory called lib. The main() method, which starts the application, is part of the Dart code included in the main.dart file. This application was created to acquaint you with the steps involved in creating and organising a Flutter application. 

USING HOT RELOAD  

Flutter’s hot reload helps you see code and user interface changes immediately while retaining state to an app running the Dart virtual machine. In other words, every time you make code changes, you don’t need to reload the app, because the current page shows the changes immediately 

To see how hot reload works, you’ll start the emulator/simulator, make changes to the page title, save them, and see the changes happen immediately. The theme widgets are a great way to style and define global colors and font styles for your app. There are two ways to use theme widgets—to style the look and feel globally or to style just a portion of the app. For instance, you can use themes to style the color brightness (light text on a dark background or vice versa); the primary and accent colors; the canvas color; and the color of app bars, cards, dividers, selected and unselected options, buttons, hints, errors, text, icons, and so on. 

 

Using a Global App Theme 

Let’s take the new ch2_my_counter app and modify the primary color. The current color is blue, so let’s change it to light green. Add a new line below the primarySwatch and add code to change the background color (canvasColor) to lightGreen. This can be done in reverse by using TargetPlatform. Specifically, to show Android traits on iOS, change the platform property to TargetPlatform.android and run the app from the iOS simulator. The app bar’s title is not center aligned but has changed to be left aligned, which is the customary Android style 

To override the app-wide theme, you can wrap widgets in a Theme widget. This method will completely override the app ThemeData instance without inheriting any styles. you changed primarySwatch and canvasColor to lightGreen, which affected all widgets in the app. What if you want only one widget on a page to have a different color scheme and the rest of the widget. Extending the app parent theme, changing only the properties needed and inheriting the rest. Use the copyWith method to create a copy of the app parent theme and replace only the properties that you need to change. Breaking it down 

 USING EXTERNAL PACKAGES 

Sometimes it’s not worth building a widget from scratch. Flutter supports third-party packages for the Flutter and Dart ecosystems. Packages contain the source code logic and are easily shared. Dart packages are written in Dart and may contain Flutter-specific dependencies Plugin packages are written in Dart (with the Dart code exposing the API) but are combined with platform-specific code implementations for Android (Java or Kotlin) and/or iOS (Objective-C or Swift). Most plugin packages aim to support both Android and iOS. By adding the shared_preference dependencies in the pubspec.yaml file, the dependencies are downloaded to the local project. Use the import statement to make the shared_preference package available.  

I've only recently begun to develop Flutter apps! It's a time-saver; I've learnt how to make my first app and use hot reload to see changes fast. Additionally, I saw how themes can be used to style apps and when stateful or stateless widgets should be used. Additionally, I learnt how using third-party packages might help me avoid starting from scratch. I have a solid understanding of the fundamental concepts underlying Flutter programming, even though I'm not yet concentrating on delving deeply into the code. 

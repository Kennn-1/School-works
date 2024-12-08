# School-works
Flutter is Google’s portable UI framework for building modern, native, and reactive applications for iOS and Android. Google is also working on Flutter desktop embedding and Flutter for the Web (Hummingbird) and embedded devices (Raspberry Pi, home, automotive, and more). Flutter uses Dart to create your user interface, removing the need to use separate languages like Markup or visual designers. Flutter is declarative; in other words, Flutter builds the UI to reflect the state of the app. When the state (data) changes, the UI is redrawn, and Flutter constructs a new instance of the widget. 

Flutter is an open-source UI software development toolkit created by Google. It enables developers to build natively compiled applications for multiple platforms, including Android, iOS, Web, and Desktop, all from a single codebase. Flutter is known for its high-performance rendering engine and a declarative UI framework that simplifies creating beautiful and responsive user interfaces. 

 

The Flutter UI is implemented by using widgets from a modern reactive framework. Flutter uses its own rendering engine to draw widgets. In Chapter 5, “Understanding the Widget Tree,” you’ll get an introduction to widgets, and in Chapter 6, “Using Common Widgets,” you’ll learn how to implement widgets. You might be asking, what is a widget? Widgets can be compared to LEGO blocks; by adding blocks together, you create an object, and by adding different kinds of blocks, you can alter the look and behavior of the object. Widgets are the building blocks of a Flutter app, and each widget is an immutable declaration of the user interface. In other words, widgets are configurations (instructions) for different parts of the UI. Placing the widgets together creates the widget tree. 

 To build the UI, you use two main types of widgets, StatelessWidget and StatefulWidget. A stateless widget is used when the values (state) do not change, and the stateful widget is used when 

A StatelessWidget is built based on its own configuration and does not change dynamically. For example, the screen displays an image with a description and will not change. The stateless widget is declared with one class 

Although a StatefulWidget is constructed using its own configuration, it is subject to dynamic modification. For instance, the screen shows a symbol and a description, but the user's actions, such as selecting a new icon or description, might alter the values. The changeable state of this kind of widget is subject to alter over time. The State class and the StatefulWidget class are the two classes used to declare the stateful widget. When the widget's configuration changes, the StatefulWidget class is recreated, but the State class can persist (remain), improving speed. For instance, the widget gets recreated whenever the state changes. A new State object is produced if the StatefulWidget is taken out of the tree and then put back in at a later time. Keep in mind that under some 

Elements are responsible for assessing the differences between widgets and maintaining a reference to the widget. Elements are created for each child widget when a widget is in responsible of producing them.  

child widget. When BuildContext objects are utilised, they are represented as Element objects.  

The BuildContext interface is used to prevent direct manipulation of Element objects.  

 

rather. The Flutter framework uses BuildContext objects to dissuade you from altering Element objects. To put it another way, you'll create your UI layouts using widgets, but  

Understanding the architecture and internal workings of the Flutter framework is advantageous. 

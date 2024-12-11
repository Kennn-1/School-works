How to use basic widgets such as Scaffold, AppBar, SafeArea, Container, Text,
RichText, Column, and Row, as well as different types of buttons, How to nest the Column and Row widgets together to create different UI layouts When building a mobile app, you’ll usually implement certain widgets for the base structure.
Being familiar with them is necessary
Scaffold As you learned in Chapter 4, “Creating a Starter Project Template,” the Scaffold widget implements the basic Material Design visual layout, allowing you to easily add
various widgets such as AppBar, BottomAppBar, FloatingActionButton, Drawer, SnackBar, BottomSheet, and more.
AppBar The AppBar widget usually contains the standard title, toolbar, leading, and
actions properties (along with buttons), as well as many customization options.
title The title property is typically implemented with a Text widget. You can customize it with other widgets such as a DropdownButton widget.
leading The leading property is displayed before the title property. Usually this is an
IconButton or BackButton.
actions The actions property is displayed to the right of the title property. It’s a list
of widgets aligned to the upper right of an AppBar widget usually with an IconButton or
PopupMenuButton.
SafeArea The SafeArea widget is necessary for today’s devices such as the iPhone X or
Android devices with a notch (a partial cut-out obscuring the screen usually located on
the top portion of the device). The SafeArea widget automatically adds sufficient padding
to the child widget to avoid intrusions by the operating system. You can optionally pass a
minimum amount of padding or a Boolean value to not enforce padding on the top, bottom,
left, or right.
Container The Container widget is a commonly used widget that allows customization
of its child widget. You can easily add properties such as color, width, height, padding,
margin, border, constraint, alignment, transform (such as rotating or sizing the widget),
and many others. The child property is optional, and the Container widget can be used as
an empty placeholder (invisible) to add space between widgets.
Text The Text widget is used to display a string of characters. The Text constructor takes
the arguments string, style, maxLines, overflow, textAlign, and others. A constructor is
how the arguments are passed to initialize and customize the Text widget.
RichText The RichText widget is a great way to display text using multiple styles. The
RichText widget takes TextSpans as children to style different parts of the strings.
Column A Column widget displays its children vertically. It takes a children property containing an array of List<Widget>, meaning you can add multiple widgets. The children align
vertically without taking up the full height of the screen. Each child widget can be embedded
in an Expanded widget to fill the available space. CrossAxisAlignment, MainAxisAlignment, and MainAxisSize can be used to align and size how much space is occupied on the
main axis.
I can customize the AppBar widget in Flutter by using widgets to modify properties like the title, leading, toolbar, and actions. For example, I can set the title to a custom widget like Text or Row, add a custom IconButton to the leading property for navigation, and use the actions property to add buttons like search or notifications. Additionally, I can adjust the toolbar’s height and background color to match the app's design. The SafeArea widget is a must for today’s devices such as the iPhone X or Android devices with a
notch (a partial cut-out obscuring the screen usually located on the top portion of the device). The
SafeArea widget automatically adds sufficient padding to the child widget to avoid intrusions by the
operating system. You can optionally pass minimum padding or a Boolean value to not enforce padding on the top, bottom, left, or right.
A Column widget displays its children
vertically. It takes a children property containing an array
of List<Widget>. The children align vertically without taking up the full height of the screen.

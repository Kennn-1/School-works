In this chapter, I'll learn that navigation is a key component of a mobile app. Good navigation enhances the user experience (UX) by making it easy to find and access information. For instance, if I’m making a journal entry and need to select a tag, but the tag isn’t available, good navigation would allow me to easily create a new one without frustration.
The Navigator widget manages a stack of routes to move between pages. You can optionally pass
data to the destination page and back to the original page. To start navigating between pages, you use
the Navigator.push, pushNamed, and pop methods. (You’ll learn how to use the pushNamed method
in the “Using the Named Navigator Route” section of this chapter.) Navigator is incredibly smart; it
shows native navigation on iOS or Android The project has a main home page with a FloatingActionButton to navigate to a gratitude page by
passing a default selected Radio button value. The gratitude page shows three Radio buttons to select
a value and then pass it back to the home page and update the Text widget with the appropriate value.
The AppBar has an actions IconButton that navigates to the about page by passing a fullscreenDialog argument set to true to create a full-screen modal dialog. The modal dialog shows a close button
at the upper left of the page and animates from the bottom. In this first part, you’ll develop the navigation from the main page to the About page and back.
Navigator is simple to use but also powerful. Let’s examine how it works. Navigator.push() passes
two arguments: context and MaterialPageRoute. For the first argument, you pass the context argument. The second argument, MaterialPageRoute(), gives you the horsepower to navigate to another
page using platform-specific animation. Only the builder is required to navigate with the optional
fullscreenDialog argument.
The second part of the app is to navigate to the gratitude page by passing a default value to select the
appropriate Radio button. Once you navigate back to the home page, the newly selected Radio button
value is passed back and displayed in the Text widget.
To receive data passed from the home page, modify the Gratitude class by adding a final int
variable named radioGroupValue. Note the final variable does not start with an underscore. Create a named constructor requiring this parameter. 
The Row children list of Widget contains three alternating Radio and Text widgets. The Radio
widget takes the value, groupValue, and onChanged properties. The value property is the ID
value for the Radio button. The groupValue property holds the value of the currently selected
Radio button. The onChanged passes the selected index value to the custom method _radioOnChanged() that handles which Radio button is currently selected. Following each Radio button,
there is a Text widget that acts as a label for the Radio button.
An alternate way to use Navigator is to refer to the page that you are navigating to by the route
name. The route name starts with a slash, and then comes the route name.
The Hero widget is a great out-of-the-box animation to convey the navigation action of a widget
flying into place from one page to another. The hero animation is a shared element transition (animation) between two different pages.
To visualize the animation, imagine seeing a superhero flying into action. For example, you have a list
of journal entries with a photo thumbnail, the user selects an entry, and you see the photo thumbnail
transition to the detail page by moving and growing to full size
the Hero widget has an Icon as a child wrapped in a GestureDetector. An InkWell
could also be used instead of the GestureDetector to show a material tap animation. The InkWell
widget is a Material Component that responds to touch gestures by displaying a splash (ripple) effect.
Add to the GestureDetector child a Hero widget with tag 'format_paint'; tag can be any
unique ID. The Hero widget child is a format_paint icon with lightGreen color and a size
value of 120.0 pixels. Note you could have used an InkWell() widget instead of
GestureDetector(). The InkWell() widget shows a splash feedback where tapped, but the
GestureDetector() widget will not show the touch
The hero animation is a powerful built-in animation to convey an action by automatically animating a
widget from one page to another to the correct size and position. On the home page, you declare a
GestureDetector with the Hero widget as the child widget. The Hero widget sets an Icon as the
child. The onTap calls the Navigator.push() method, which navigates to the page Fly.
BottomNavigationBar is a Material Design widget that displays a list of BottomNavigationBarItems that contains an icon and a title at the bottom of the page.. When the BottomNavigationBarItem is selected, the appropriate page is built
The BottomNavigationBar items property has a List of three BottomNavigationBarItems. For
each BottomNavigationBarItem, you set an icon property and a title property. The Bottom­ NavigationBar onTap passes the selected index value to the _changePage method. The _changePage
method uses setState() to set the _currentIndex and _currentPage to display. The _currentIndex
sets the selected BottomNavigationBarItem, and the _currentPage sets the current page to display
from the _listPages List.
The BottomAppBar widget behaves similarly to the BottomNavigationBar, but it has an optional
notch along the top. By adding a FloatingActionButton and enabling the notch, the notch provides
a nice 3D effect so it looks like the button is recessed into the
navigation bar.
The TabBar widget is a Material Design widget that displays a horizontal row of tabs. The tabs
property takes a List of Widgets, and you add tabs by using the Tab widget. Instead of using the
Tab widget, you could create a custom widget, which shows the power of Flutter. The selected Tab is
marked with a bottom selection line.
When TabBar and TabBarView are used together, the correct associated page is automatically loaded.
When the user swipes the TabBarView left or right, it scrolls to the correct page and selects the corresponding tab in the TabBar. All of these powerful features are built in; no custom coding is necessary
Drawer is a Material Design panel that slides horizontally from the left or right edge of the Scaffold,
the device screen. Drawer is used with the Scaffold drawer (left-side) property or endDrawer (rightside) property. Drawer can be customized for each individual need but usually has a header to show
an image or fixed information and a ListView to show a list of navigable pages.

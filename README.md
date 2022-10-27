# For_TATA_Digital

1)Can we nest the Scaffold widget? Why or Why not?

Yes we can use nested Scaffold widget, But not recommended to do so. Just take and example.

import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    title: 'Navigation Basics',
    home: FirstRoute(),
  ));
}

class FirstRoute extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('First Route'),
      ),
      body: Scaffold(
        body: Center(
          child: RaisedButton(
            child: Text('Open route'),
            onPressed: () {},
          ),
        ),
      ),
    );
  }
}

Here, we are nesting two Scaffolds, and, as you can see, the second app bar is being drawn below the first app bar. That would not be the best approach for tabbed or nested navigations. 

2)What are the different ways we can create a custom widget?

Basically flutter has two types of states. First is State full and second is stateless. We can create widget by using both way. 

We can create widget in same class also can create on separate class.

Hope you got the answer. 

3)How can I access platform(iOS or Android) specific code from Flutter? 

By using Method on platform Channel

4)What is BuildContext? What is its importance?

A BuildContext is nothing else but a reference to the location of a Widget within the tree structure of all the Widgets which are built.





5)Refactor the code below so that the children will wrap to the next line when
the display width is small for them to fit.

Just wrap it with Wrap()

Example.

return Wrap(
      children: <Widget>[
        new RaisedButton(child: const Text('Foo')),
        new RaisedButton(child: const Text('Foo Bar')),
        new RaisedButton(child: const Text('Foo Bar Bas')),
        new RaisedButton(child: const Text('F')),
        new RaisedButton(child: const Text('B'))
      ],
);

6)Identify the problem in the following code block and correct it.

There is no problem in code only problem is it could generate performance issue. That’s it.

7)In the below code, list1 declared with var, list2 with final and list3 with const.
What is the difference between these lists? Will the last two lines compile?

In given code snippet while assigning value to final list[2] = ‘dart’ will generate error coz we can not update final variable.

While assigning value to const it will generate error coz we have to initialize it before and we can not edit it further.

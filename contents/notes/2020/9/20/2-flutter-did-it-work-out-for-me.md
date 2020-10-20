I have been building applications formally (professionally) since 2007. Although, I started application development in1995. I have seen the evolution of application development from basic PHP functions with raw SQL queries to sophisticated and mature frameworks (Angular, Vue.js, Flutter, Rails, etc)

So, did Flutter work out for me?
Yes! But why?

We all have been developing web applications and websites for the longest time. And one of the main aspects of web development is that it is extremely “quick” to view changes in the code, during development. Either we reload the web page to view the changes or we open Firebug and test changes on the fly. In short, any changes to the code is reflected, next to real-time. We always wanted and built libraries and frameworks to bring more discipline and structure to our code, but we never needed a “quicker” way to view changes.

This is were Flutter is incredible: While we are editing our code, we can “hot reload” the state of the application, which does not restart the application, it “automagically” re-renders the current screen. We can also “hot reload” the entire app, neither of which compiles, builds and then executes it. It just updates the screen!

Let us see how Flutter scores on the following:

## 1. Development Speed: 👍
Probably the fastest I have seen, including web frames which can auto-detect file changes and reload the webpage.

Hint: See that you have the “editor”, “terminal” and “simulator” all visible at the same time on the screen. Then you can pretty much edit code while looking at the simulator.

![Flutter Side Windows](https://i.imgur.com/l15x1tG.png)


### 2. Cross Platform 👍

Yes! It generates an .ipa and an .apk perfectly. With almost identical rendering on both platforms. Flutter is not a web container, nor does it use the platform’s rendering engine (or widget stack). Flutter has its own rendering engine, it has defined it widgets stack, state management and layouts.

Hint: Spend some time reading up the widget catalog. There are many widgets out there to boilerplate your application, and you might even find yourself using them in production as well.

### 3. Code Verbosity 👎

Unless you are continuously modularising code into separate files, you will very quickly find yourself with extremely long files, could even go up to 1000 lines, or more!

Dart, to me, is a very “pretty” language. But the way the UI is implemented can make the code look quite overwhelming!

### 4. Programming Language: Dart 👍

Dart is a programming language designed for client-side development. I love the language, love the features. My favorite would be <Future> ! It definitely is the future of the hybrid of synchronous and asynchronous development.

Would I build a production application with Flutter?
We released The Monk late May 2019. It took about 3 months to finish development. It renders beautifully and is extremely snappy.

We knew the choice would be to build the application using a cross-platform framework, and as I have built other applications using ReactNative, I was leaning towards it. But after reading up enough about Flutter, it really won me over and I was willing to take the risk with the new technology, for a large scale production application. It totally paid off!

Now, will it pass the test of time? I think it will, it has done great so far, and is evolving quite beautifully.

![The Monk](https://i.imgur.com/oLf19NK.png)
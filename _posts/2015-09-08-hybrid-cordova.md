---
layout: post
title: Hybrid App Development
excerpt: I do not have as much experience in mobile development as I would like. Although I am very comfortable with responsive design using JS and CSS I want to dive deeper into mobile development. Since getting my MacBook I’ve spent a little time in Xcode and doing a couple of ‘hello world’ things and playing with Swift but nothing too serious. I’ve heard Ionic and Cordova mentioned a few times lately and so I’m going to take a look. I’ll probably continue to learn some of the native Swift/Objective-C/Java features, but given how much fun Javascript has been lately going with a hybrid solution just seems good.
---

I do not have as much experience in mobile development as I would like. Although I am very comfortable with responsive design using JS and CSS I want to dive deeper into mobile development. Since getting my MacBook I’ve spent a little time in Xcode and doing a couple of ‘hello world’ things and playing with Swift but nothing too serious. I’ve heard Ionic and Cordova mentioned a few times lately and so I’m going to take a look. I’ll probably continue to learn some of the native Swift/Objective-C/Java features, but given how much fun Javascript has been lately going with a hybrid solution just seems good.

#What is Cordova?
Cordova exposes many of the native device features through Javascript APIs.
>[Apache Cordova](http://cordova.apache.org/docs/en/5.0.0/guide_overview_index.md.html#Overview) is an open-source mobile development framework. It allows you to use standard web technologies such as HTML5, CSS3, and JavaScript for cross-platform development, avoiding each mobile platforms' native development language. Applications execute within wrappers targeted to each platform, and rely on standards-compliant API bindings to access each device's sensors, data, and network status.

#Getting Cordova
To install Cordova all you need to have is [Node.js](https://nodejs.org/)
{% highlight bash %}
$ sudo npm install -g cordova
{% endhighlight %}

#Create the App
{% highlight bash %}
$ cordova create iterative com.iterative.hello HelloWorld
{% endhighlight %}

This will generate the skeleton project in a directory called iterative. The second and third arguments are optional. The second argument is an identifier and the third is the applications display title.

#Add the iOS platform
{% highlight bash %}
$ cd iterative #make sure you are in the directory
$ cordova platform add ios
{% endhighlight %}

You could also do android, windows8, etc...
{% highlight bash %}
$ cordova platform add amazon-fireos
$ cordova platform add android
$ cordova platform add blackberry10
$ cordova platform add firefoxos
{% endhighlight %}

![Screenshot](/public/images/8705FB8C-A532-4D0E-88D8-8AA55C9A3C0F.png "Screenshot")
Looks like the iOS folder is created with all of the necessary setup files.

![Screenshot](/public/images/F50E7D30-E4E0-4DCA-B447-2FD2E2226DFB.png "Screenshot")
This is the project opened in Xcode. The www directory contains the stuff I am most curious about: the HTML/CSS/JS. I’m going to go ahead a make a couple of small changes: replace logo.png with my own and put in some different text. Small changes but just to see if it picks them up.

#Build the App
{% highlight bash %}
$ cordova build
{% endhighlight %}

This will compile everything from the www directory to the specific platform. If I make any changes to the www files, as I did, you just need to run this again to compile it down the platform specific folders.
Now I can either jump back into Xcode and click Run or do this
{% highlight bash %}
$ cordova emulate
{% endhighlight %}

![Screenshot](/public/images/79B7F8A7-0D62-4366-82E2-17399D127DC5.png "Screenshot")
And here is my new Cordova App running in the iOS simulator.

It is surprisingly simple to get up and running with Cordova. Just getting this far in such a short amount of time has made me far less intimidated with rich mobile development. I'm looking forward to Ionic!

#Links
[Cordova](https://cordova.apache.org/)

[The Command-Line Interface (CLI)](http://cordova.apache.org/docs/en/3.4.0/guide_cli_index.md.html#The%20Command-Line%20Interface)

[Getting Started with Visual Studio Tools for Apache Cordova](https://msdn.microsoft.com/en-us/library/Dn771545.aspx)
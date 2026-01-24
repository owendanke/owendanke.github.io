---
layout: post
title: Working On An App!
description: WIP Flutter app
date: 2026-01-24
tags: [projects,coding]
---

![Image](/assets/images/IMG_7053.jpg)

As the title suggests, I am working on an app. The app is for a local non-profit's arboreteum, the Holcomb Farm Tree Trail.
Please ignore the crappy images, I didn't feel like figuring out screenshots.
For this project I decided to use Flutter, a cross platfrom app framework that uses Dart. I gave React a try but I found it frusturating since it is very similar to HTML. Flutter, on the other hand, is much more familiar to me as Dart is similar to Java and C (in my opinion). 

The problem I faced at the start was not knowing Dart, this has since diminished, but my competency with Dart is much better.
Issues with asynchronous functions like race conditions still get find their way into the code, like forgetting that darn `await` keyword. That sucker doesn't stand out in hunderds of lines of async file handling.
This app has been in the works for a few months (on and off) and I have been learning Dart through this Flutter app.
I haven't made any non-Flutter Dart programs, but the next tool I need will be written with Dart.

![Image](/assets/images/IMG_7051.jpg)

Currently the app has some pages about Holcomb Farm and the Tree Trail, a list of trees that are planted with descriptions and pictures, and as of writing this page a working map!
The UI styling needs some work, it feels a little lackluster, but I have been more focused on the back-end details.
Many UI/UX aspects of the app are programmatically laid out. The tree list, for example, is built from an actual list. There are constructors that define how the different pages look and the app builds them based on which trees it know of.

![Image](/assets/images/IMG_7049.jpg)

Another really convenient feature this app has is the asset management. 
Nearly all the assets used in the app are hosted on the cloud and locally cached.
When the app is launched it checks for local files and if there are none it attempts to download them from the cloud storage.
What this achieves is the ability to continuously update content on the app without pushing an update.
Of course for major changes such as UI, functionality, and the type of content will still require a app store update.


This is just a small update and introduction to the project, there will be more posts!
Oh, and the app will be open-source, but as I am in the learning process right now I don't want to release any sensitive information such as API keys.
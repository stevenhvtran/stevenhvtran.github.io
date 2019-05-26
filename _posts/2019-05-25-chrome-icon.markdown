---
layout: post
title:  "Chrome's Annoying Icon"
date: 25/05/2019 9:44:26 PM 
categories: [misc]
---

# The Problem
Chrome's Start Menu icon always bugs me. It's slightly too large and the
background colour clashes with the theme. Here's a screenshot of the problem:

![start-menu](/assets/start-menu.png){: .center-image }

# The Fix
1. Search for Notepad in your Start Menu
2. Right click Notepad and select `Run as administrator`
3. Open `C:\Program Files (x86)\Google\Chrome\Application\chrome.VisualElementsManifest.xml`
4. Change this line `BackgroundColor='#5F6368'/>` to
   `BackgroundColor='transparent'/>` and save the file
5. Right click the Chrome icon in the Start Menu, `More > Open file location`
6. Right click the Chrome shortcut, `Properties > Change Icon...`
7. Click `Okay` without changing the icon

# Results
As you can see the Chrome icon is now the right size and colour with a change
of a single variable

![fixed-start-menu](/assets/fixed-start-menu.png){: .center-image }

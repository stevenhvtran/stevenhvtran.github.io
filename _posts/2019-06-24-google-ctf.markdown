---
layout: post
title:  "My Attempt At Google CTF for Beginners"
date: 24/06/2019 2:29:00 pm
---

# The Challenge
Google CTF seemed like a cool challenge so I attempted to solve it this year,
having never attempted a CTF before.

The website for the CTF can be found [here](https://capturetheflag.withgoogle.com/)

# My Solutions

## Problem 0
- The first problem had an attachment that when unzipped had two files,
  `log.txt` and `rand2`
- `log.txt` contained random co-ordinates whilst `rand2` contained a jumble
  of text when opened in vim
- By doing a search in `rand2` for `CTF` in vim, we find the first flag
![Flag 0](/assets/google-ctf/flag-0.png){: .center-image}

## Problem 1
- On the second problem I was redirected to a YouTube video advertising the
  CTF competition [here](https://www.youtube.com/watch?v=QzFuwljOj8Y)
- At `0:17`, moving frame-by-frame using `,` and `.` keys, we can see the next
  flag
![Flag 1](/assets/google-ctf/flag-1.png){: .center-image}

## Problem 2
- The next problem was more tricky and required some more domain knowledge
- The zip file contained 2 files this time, `init_sat` and `README.pdf`
- `README.pdf` contained an image of a satellite with a useful name in it,
  *Osmium*
![Flag 2.0](/assets/google-ctf/flag-2.0.png){: .center-image}
- After looking around the contents of `init_sat` I realised it was an
  executable file in Linux, running it on Linux results in a terminal-like UI
![Flag 2.1](/assets/google-ctf/flag-2.1.png){: .center-image}
- Opening the Google Docs URL leads to a plain document with just some jumble
  of text
![Flag 2.2](/assets/google-ctf/flag-2.2.png){: .center-image}
- A common reversible encoding of text is `Base64` - so after running the text
  through a decoder we get some hints
![Flag 2.3](/assets/google-ctf/flag-2.3.png){: .center-image}
- By re-running `init_sat` again with Wireshark open this time we can examine
  network activity and sniff for any calls made by the program on our network
- After looking around we can find some calls that go to
  `satellite.competition.com`, by doing `Follow > TCP Stream` we can see what
  the communications are in plain text
![Flag 2.4](/assets/google-ctf/flag-2.4.png){: .center-image}
- The flag is finally revealed here

## Problem 3
- Coming as soon as I can work it out...

+++
date = "2017-07-19T15:18:28+05:30"
description = ""
featured_image = ""
tags = []
title = "Integrating Pocketsphinx.js - Week 7"

+++

This entire week has been devoted to adding Pocketsphinx.js recognizer to the application. The first thing we had to decide was whether to put a separate recognizer for the entire application.

Most of this week has been spent trying to implement the application that I made in March into the Twine HTML files. This hasn't working and has been incredibly buggy resulting in the microphone not working at all and has delayed my schedule for the week. The way Flask handles such features might be slightly different form pure HTML/JavaScript files so I have been trying to implement my recognizer in pieces. I've stripped away most of the styling and only left the record button along with the replay and evaluate button. I'm hoping that building it again from the ground up will let me find the problem.

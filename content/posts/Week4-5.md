+++
date = "2017-07-08T18:27:38+05:30"
description = ""
featured_image = ""
tags = []
title = "Using Python Flask - Week 4&5"

+++

I've decided to combine these 2 weeks as it seems to make more sense as not much was accomplished during week 4.

Right now I have to make a flask application which wraps around the Twine Stories that I've already used. This is the first step towards making the final Computer Aided Learning Interface. Right now the Twine stories are purely navigated through by just clicking on the correct option. The whole point of this project is to be able to do this by the means of speech recognition and to give feedback on this. This requires another application to be built around Twine which in this case will be [Python Flask](http://flask.pocoo.org/docs/0.12/).

Flask is often referred to as a micro framework. It aims to keep the core of an application simple yet extensible. Flask does not have built-in abstraction layer for database handling, nor does it have form a validation support. Instead, Flask for each different function I have to add the relevant extension. This keeps it lightweight and highly customizable whatever I need to add. Since I don't have all the data for the voice recordings yet I have to build a prototype without it and account for it to be integrated later. This means that I have to first make the basic navigation using Flask without just a submit button. Later this submit button will also have a web recorder next to it. The web recorder will record and process the voice response and then on clicking the submit button, Pocketsphinx.js will process it and grade the voice response.

I have already made the Twee files that will be used for parsing and just need to make a python program which can extract the responses. I have to now replace the buttons with a Pocketsphinx.js recognizer expecting the correct button label.

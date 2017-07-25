+++
date = "2017-07-15T00:18:42+05:30"
description = ""
featured_image = ""
tags = []
title = "Flask and making parsers - Week 6"

+++

Using Flask has been a bit slow as I've had to learn an entirely new framework. Flask applications work on connecting different HTML pages through code which acts as a wrapper.

The first thing that I had to do was make a parser for the which separates all the Twine pages into HTML files. Separating the files was important as it would make the routing between pages much more streamlined using the Flask application. The files were named corresponding to their node name. For example, the beginning file was named "Start.html". The next file was name "Step1.html" and the failure response file was named "End0.html". Naming them in this fashion will be uniform throughout every single Twee file which means I don't have to change any code in the Flask application when I'm loading a different Twine story. It also doesn't matter how long the Twin story is or how many options are present which makes it scalable.

After making the HTML files, the JSGF files related to each response had to be made. This was also done using a parser which selected the responses from the Twee file and then looked up the corresponding pronunciations from the dictionary.

The JSGF format would be: public <choice> = [ phoneme string 1 |
phoneme string 2 | phoneme string 3 ]

These files will then be loaded into Pocketsphinx.js at the time of running of the application and will be used to distinguish between the responses. The user will press a button to record his response. The Javascript code will then read the response and send back the corresponding option as a POST request. The Flask application will receive this request and then process it. The information that will be sent in the POST request will be the name of the next node corresponding to the option selected. This name will then be directly used by the Flask application to route the next HTML file as all the file names will be based on their node. This process will continue until the user reaches the end of the scenario or quits.

As of now I have finished making the two Python parsers and also the basic Flask application. The navigation right now is done using buttons while I start integrating Pocketsphinx.js

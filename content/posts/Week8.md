+++
date = "2017-07-24T00:18:52+05:30"
description = ""
featured_image = ""
tags = []
title = "Pocketsphinx.js - Week 8"

+++

From the previous week my main aim was to implement a basic version of the recognizer from [syl22-00/pocketsphinx.js](https://github.com/syl22-00/pocketsphinx.js). I have built a previous version of it earlier which I used as a basic from [SND96/pocketsphinx-scores](https://github.com/SND96/pocketsphinx-scores). I originally built this to to get the alignment scores for words in the phrase "What's your name?". I won't need this for now so I removed that completely but may include it at a later time when the application is more stable.

 The features that I did add to the original Pocketsphinx.js application were a playback system which needed the use of [Recorder.js](https://github.com/SND96/pocketsphinx-scores). This playback system will be necessary if the user of the application wishes to hear his pronunciation so that he can correct his mistakes. There is only one Pocketsphinx.js recognizer which will record the user's response and will then take them to the next page in the Twine story based on the option which he has selected. As a placeholder for the responses the user just has to say either "One","Two" or "Three" corresponding to the option he wants to select. The user's response will be recorded using Recorder.js that I had mentioned earlier. I'm going to be using this while I debug the rest of the system. Once this is done I will replace the generic option responses with the specific responses for each node in the Twine story. The JSGF files for these responses have already been created so they have to only be loaded into Pocketsphinx.js  

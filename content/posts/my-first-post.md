+++
date = "2017-06-20T20:26:48+05:30"
description = ""
featured_image = "Gsoc-logo.jpg"
tags = []
title = "Introduction - Week 1"
+++
Hi everyone! My name’s Sahith Dambekodi and I’m a second year undergrad student at [BITS Pilani K.K. Birla Goa Campus](http://www.bits-pilani.ac.in/Goa/). I’m pursuing a major in Electrical and Electronics engineering.

My initial foray into open source began mainly with general purpose machine learning libraries like scikit-learn and tensorflow. I had heard about Google Summer Of Code through my peers and I was intrigued  by the possibilities of coding an entire summer about something I was genuinely interested in. This led me to [CMUSphinx](https://cmusphinx.github.io), which is an open source speech recognition system for mobile and server applications. Its an offline system which is useful in applications where internet isn’t reliable. PocketSphinx is a version of the system built to run on smaller devices like mobile phones. I submitted my proposal to the organization and was very excited when it got selected.

What I am going to be working on in the summer is part of a larger project whose main aim is Intelligibility Remediation for non-native speakers of English. This is going to extend to a bigger Computer Assisted Pronunciation Training system. Many of these types of systems today have bottlenecks and limitations as they are still heavily dependent on human intervention.

On to the basic crux of the system itself. We will use Wikiversity and Wiktionary to add structure, flexibility and increase the size of the learning audience. Users will be able to register on the sites and track their progress while allowing the system to provide higher quality feedback. These courses will be integrated with Twine, a software from [twinery.org](http://twinery.org/), to create branching scenario assignments in the instructional ecosystem.

These are the main milestones that the project hopes to complete:

1. **Twine System/Integration:** A Twine system will be incorporated, tested for its stability and integrated with an OAuth registration system like, Moodle, Wikimedia Tool Labs LDAP authentication etc. The user’s progress can be tracked using D3.js for attractive visualizations. Twine story will be displayed with multimedia graphic, video, sound, or audiovisual presentations.

2. **Audio Recorder:** Create a system that records the audio. The audio is then transcribed and stored e.g. via forms such as [http://talknicer.com/recdemo](http://talknicer.com/recdemo) and [https://snd96.github.io/pocketsphinx-scores/live.html](https://snd96.github.io/pocketsphinx-scores/live.html) and [https://jsalsman.github.io/transcriber-qualification](https://jsalsman.github.io/transcriber-qualification/) and [http://talknicer.com/d/index.cgi?addphrase](http://talknicer.com/d/index.cgi?addphrase) among others. Exemplar and non-exemplar audio recordings will be associated with several transcription attempts from both L1 and L2 transcriptionists.

3. **Speech Processing:** Using the recordings, process the data to get speech recognition results.

4. ** Motivation System:** To keep the user engaged and to prevent boredom or complacency, implement a system which measures the motivation of the user (du Boulay, B., & del Soldato, B.,(2016). [Implementation of Motivational Tactics](http://users.sussex.ac.uk/~bend/papers/motivation-revised2.pdf)). The user’s motivation to learn will be quantified based on 3 variables:                                  

  * **Effort (e)** can be defined as the learner’s perseverance to solve a difficult problem.

  * **Confidence (c)** can be measured using the number of skips that learner choose to do and the amount of help requested by them.

  * **Independence (i)** is measured by the amount of help requested from the systems.

5. **Community Features:** If time allows, the motivation system detailed above could also be gamified; i.e. the user’s progress can be made in the form of a role-playing game. A community feature can also be built on this like the formation of a study group.

To start out with, initial questions and scenarios will be designed to instruct how to use one of last year’s GSOC projects, the [“Accuracy Review of Wikipedias in Flask”](https://tools.wmflabs.org/arowf/) system . These questions will be written in Twine format and displayed to the user for interactive assessment and instruction. These scenarios will require the user to speak into the browser microphone and [Pocketpshinx.js](https://github.com/syl22-00/pocketsphinx.js) will help identify the words being spoken.

I’m happy to have James Salsman as my mentor for this project along with the community from CMUSphinx. Looking forward to a productive summer ahead!
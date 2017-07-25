+++
date = "2017-06-27T11:28:37+05:30"
description = ""
featured_image = ""
tags = []
title = "Speech Processing - Week 3"

+++

This third week has been devoted mainly to processing the necessary prompt files which will be used later for the the education system. There were two different types of recordings. One which had purely a single word. These proved challenging in the beginning but we soon managed to process the files using the correct commands in sphinx.

The first step was converting all the files into .wav(16,000 samples per second, 16 signed bits per sample, little endian) format from .mp3 as sphinx works with files only in this format. The next step was getting -align.txt files for them according to [https://cmusphinx.github.io/wiki/pocketsphinx_pronunciation_evaluation/](https://cmusphinx.github.io/wiki/pocketsphinx_pronunciation_evaluation/).
This first requires the creation of .jsgf files for each of the recordings. The recording were too many to do this manually (~150000 recordings) and hence it required making a script which would generate the required files from the larger cmudict-en-us.dict file which contains all the phonemes required. Once we did this, we now had the [.jsgf](https://en.wikipedia.org/wiki/JSGF) files required for making the alignment texts. From these alignment texts we made log-1 acoustic scores and duration text files. From these files the actual standard scores for each of the recordings were made which completed the speech processing required before the audio files could be properly used.

Next we have use an algorithm to find the “maximally distant” vectors of the standard scores generated. The ida is to get as wide a coverage of features as possible. My mentor James, then used R's PAM([Partitioning Around Medoids](https://en.wikipedia.org/wiki/K-medoids)) algorithm in its 'cluster' library's pam() command to select 30 medoid recordings for each of the 82 words after which they can be put up onto Amazon Mechanical Turk so that more information can be gathered from them. PAM algorithm uses a greedy search which may not find the optimal solution but is faster than an exhaustive search.

This has been done for single word recordings and now I am working on the multiple word recordings. I have managed to get the .jsgf files required by trawling through the dictionary and writing the appropriate words to the file but it will take more time for me to finish the remaining steps in processing as there can be a lot of variance and disturbance in the recording.

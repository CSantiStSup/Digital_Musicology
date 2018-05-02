---


---

<h1 id="milestone-3">Milestone 3</h1>
<p>At the end of Milestone 2, we were struggling with the web scrapping part of Ultimate Guitar. Indeed there were some issues with the website. It is now fixed, and we were able to fully get the data as you can see in the notebook. As for the second handout, there are two distinct parts of this work, the text processing and chord processing.</p>
<h2 id="text-processing">Text processing</h2>
<p>Words were assembled in clauses when we extracted them, we  splitted them into individual instances. The Term Frequency-Invert Document Frequency (TF-IDF), was used once stopwords were removed. During this process we chosed to to keep only sentences which were longer than 10 words, because shorter ones are sparsed data.</p>
<p><strong>Note regarding stemming:</strong>  We chose not to stem words in this analysis because we think that stemmed words are not the most fitting form for a complexity analysis. When someone is using a word play, it can occur that forms of a specific word are employed with different meanings. For instance, ‘run’, ‘runs’ and ‘running’ could be used in 3 different ways in the same text, and stemming the 3 of them into ‘run’ will reduce the complexity score of the given piece.</p>
<p><strong>Note perfoming a readability test:</strong> Because we are dealing with song that are written by users, it most of the time lacks of punctation. Readability tests present differencies, and we looked at the following ones:</p>
<ul>
<li>Automated Readability Index</li>
<li>SMOG</li>
<li>Flesch-Kincaid Grade Level</li>
<li>Coleman Liau Index</li>
<li>Gunning Fog Index</li>
</ul>
<p>They all use the length of a sentence as a parameter, thus why with no punctuation, it is not possible to perform it on the data of this project.</p>
<h2 id="chords-processing">Chords processing</h2>
<p>At first, we had to clean and fine grain the data. During this process we took some decisions regarding the chords and what we decided to take out. Those details are given in the Notebook. We encoded all the chords with the details they present, all in one-hot encoding (binary states) in order to be able to conduct computational models on it. As in class, chord transitions were established (taking into account only the root) for the songs.</p>
<p><strong>Note regarding MIDI analysis:</strong> Because of the lack of procedure to analyse MIDI and the struggle to link this part with the rest of the work that we are doing, we decided not to work with the MIDI dataset anymore and rather focus solely on the data from ultimate guitar.</p>
<h3 id="final-remarks-for-milestone-3">Final remarks for milestone 3</h3>
<p>After conductiing this part of the work, we have some questions/concerns for the next part that we want to point out:</p>
<ul>
<li>
<p>Amongst those two parts of the analysis, is there any aspect that, methodologically speaking, seems problematic to you?</p>
</li>
<li>
<p>We have an encoding of chords that can be easily used to conduct an analysis of harmonic complexity, however we do not know exactly how we could apply a metric that corresponds to the paper analysing harmonic complexity. Do you know a way we could weight our transition difference to end up with a coherent form of analysis for harmonic complexity?</p>
</li>
</ul>


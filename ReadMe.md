---


---

<h1 id="milestone-4">Milestone 4</h1>
<p>To read the work, <strong>please go to the Milestone 4 notebook above</strong>.</p>
<p>During this part, we finished to analyse the data and presented the results. This work is dealing with complextiy, both in the harmonic progression and the lyrics. Our goal was to determine how complexity can be characterized in different genres by conducting a large scale study. To achieve such goal we had to find a methodology to quantify harmonic and lexical complexity. This process does not have the pretention to be complete, it is rather to be taken as a meaningful insight of macro-scale characterics of genres when they are confronted to complexity.</p>
<h2 id="harmonic-progression">Harmonic progression</h2>
<p>As specified in the previous milestone, we chose to keep only songs which had  4 chords or more. By this we aimed at getting rid of incomplete parts of our dataset. For some lyrics, only the main chords were given, and not necessarily in a complete way. For the sake of consistency, we chose to get rid of those chord progressions.</p>
<h3 id="complexity-measurement">Complexity measurement</h3>
<p>Once the data strcture was established, meaning the way to store the components of each chord, it was necessary to compute the transitions. To establish a value for our transitions, we chose to consider the following assumptions:</p>
<ul>
<li>The major and minor transition (from being major to not-being major, and vice-versa) are considered the same, otherwise the same measurement is counted twice.</li>
<li>Chord qualities such as suspended, augmented, or diminished are counted twice, because we consider that they are theoretically less simple than a major to minor transition.</li>
<li>We do not consider interval sequence, because the chord/note itself has to be related to the song’s key to conduct a meaningul analysis, and such element is not included in our dataset. That is the reason why the focus has been put on harmonic quality.</li>
</ul>
<h4 id="computing-complexity-2-measurements">Computing complexity: 2 measurements</h4>
<p>We considered the complexity of each transition by establishing the following variable for each song:<br>
<img src="https://lh3.googleusercontent.com/8VBtt7R8-7sStFUhH6PWXy664hnPhdrp8Fi1-2zMZpImMHaqAcwCtq5t7jLmmEZIjKA_pctg-wV2Iw" alt="&quot;First Harmonic Complexity Measurement&quot;"><br>
And in the equation, dimensions are the different non-zero qualities that a chord has. Transition of Dimension is the sum of each transition for every quality. The “+1” is an offset to avoid 0 values for this variable (which turned out to be problematic later).  And ultimately we divided by the number of transitions in order to normalize the results. Therefore, if a song had many chords with various qualities, it will be considered to be more complex with this metric.</p>
<p>Because, to us, a song with a set of more unique chords has to be considered as more complex, we believe that we had to take this aspect into account. That is the reason why we established this second metric:<br>
<img src="https://lh3.googleusercontent.com/y6TPX7QOVm-9AAKmtvpsX4CU60x0_Z6e2KjvuPrprBLOS9Uehp3zryVj2ZTXKFPRLSGOpwp-m5rqHw" alt="enter image description here"><br>
This will value songs that have more variety in their chord progression.</p>
<p>Ultimately, to combine those two measurements we thought that they should impact on each other. The two values do not have the same scale and it would devaluate Comp2 to have an addition. That is the reason why we established the following formula:<br>
<img src="https://lh3.googleusercontent.com/PYOPm81QaX1_avAJK2W_La4O0Aqp5EeudRTv6KKQhx2ZSQwsliloQ-eKqYk5W3RrhKxriHSjfX770A" alt="enter image description here"><br>
The log comes from a scaling issue that is detailed in the notebook. A multiplication is forcing the two variables to interact, and it is important so that final metric reflects those two aspects of harmonic complexity.<br>
All the considerations that one can make with the results will be explained later.</p>
<h2 id="analysis-of-lyrics">Analysis of lyrics</h2>
<p>During the previous steps, we computed a complexity score using TF-IDF, and this allowed to have a measurement for each song. The details and the faults of the process were explained before, and it is not as accurate as a manual classification of lyrics because it only takes into account the vocabulary and not the entire structure of the lyrics.</p>
<h2 id="results">Results</h2>
<p>The results and the discussion can be seen in the notebook, however some considerations are important to bear in mind when reading it. The complexity measurements that were established are far from grasping every aspect of what one could consider as a marker of complexity in music and in lyrics. The lexical complexity is only taking into the vocabulary and not sentence structures or rimes. The harmonic complexity is only dealing with transitions and not with pitch profiles and non-local dependencies of chords. All the interpretations that can be done must fully acknowledge the limits of such computation.</p>
<br>
<br>
<br>
<br>
<h1 id="milestone-3">Milestone 3</h1>
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
<p>We have an encoding of chords that can be easily used to conduct an analysis of harmonic complexity, however we do not know exactly how we could apply a metric that corresponds to the paper analysing harmonic complexity. Do you know a way we could weight our transition difference to end up with a coherent form of analysis for harmonic complexity</p>
</li>
</ul>


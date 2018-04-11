---


---

<h1 id="the-relationship-between-complexity-and-emotion-in-music">The relationship between complexity and emotion in music</h1>
<p>By Santiago Saint Supéry and Pierre-Antoine Desplaces</p>
<h2 id="milestone-2--data-gathering-preprocessing-and-basic-statistics">Milestone 2 : Data gathering, preprocessing and basic statistics</h2>
<h3 id="main-guideline-to-go-through">Main guideline to go through</h3>
<p>We worked on both the MIDI dataset and the Ultimate Guitar one, thus why there are 2 distinct notebooks to look at. You can either take a look manually in the files above or follow those links to have them in an NBviewer:</p>
<ul>
<li><a href="https://nbviewer.jupyter.org/github/CSantiStSup/Digital_Musicology/blob/master/MIDI_data_wrangling__Miletstone%202.ipynb">MIDI Data Wrangling and steps</a></li>
<li><a href="link">Ultimate Guitar Data Wrangling and steps</a></li>
</ul>
<p>Note: There is no dataset on this repository because Ultimate Guitar was directly scrapped from the site and the MIDI file is too large to be put on Github. Detailed explanations for data structures and data sources are contained in the notebooks.</p>
<br>
<h4 id="data-gathering">Data Gathering</h4>
<p>We obtained the data using web-scrapping from the ultimate guitar website to obtain a text file containing both lyrics and chords.<br>
For the MIDI, it was a downloadable file that we directly took.</p>
<p>The formats are the following (click on the links to access the datasets):</p>
<ul>
<li><a href="https://www.ultimate-guitar.com/">Ultimate Guitar</a>: text</li>
<li><a href="https://www.reddit.com/r/WeAreTheMusicMakers/comments/3ajwe4/the_largest_midi_collection_on_the_internet/">Unsorted MIDI</a>: MIDI</li>
</ul>
<h4 id="preprocessing">Preprocessing</h4>
<p>Because ultimate guitar is website for guitarists that is collaborative, it is essential to bear in mind that the quality of the content may be a problem. That is the reason why we chose to work with the top songs of the different genres. Taking the top is using songs that are reviewed and rated by many people, thus why it is more likely to be accurate. We therefore took the 400 top songs of the 13 top different genres from the ultimate guitar website.<br>
We crawled into the MIDI data and the preprocessing was done manually, we chose to have a dataset that provided enough information to allow us to work on it and was diverse enough to provide information on different genres</p>
<h4 id="basic-statistics">Basic Statistics</h4>
<p>Those elements are embedded in the notebooks.</p>
<h4 id="subsequent-steps">Subsequent steps</h4>
<p>The next task will beto conduct the complexity analysis of chords using the paper of Marsik &amp; al. that we mentioned in the first milestone. This will be done on the Ultimate Guitar Data.  We will apply TF-IDF to analyse the complexity of the vocabulary used in the lyrics. We must also find a way to analyse the complexity of MIDI files.<br>
Because we have not find any straightforward manner to analyse the MIDI format, we must keep looking for now. If nothing valuable is found until the next milestone, we will focus on the chord progression and let aside the MIDI data.</p>
<br>
<blockquote>
<p><em>The following par of the ReadMe contains Milestone 1</em></p>
</blockquote>
<h2 id="milestone-1">Milestone 1</h2>
<p>Research question and conceptual aspects of the work.</p>
<h2 id="research-question">Research Question</h2>
<p>Regardless of the quantification aspect, complexity in music is a central element. Music is constructed on a theoretical structure that allows many possibilities and variations, however many modern musical pieces are structured in a simple way. Apart from this aspect, music is a mean to share emotions, and because works have been done exploring both of those facets, we intend to explore the link between them. In this project, we aim at linking complexity and emotion in music. Our goal is to find out if and how structural complexity in music writing in its broadest sense - that is to say for both instruments and lyrics - can have an impact on the emotional valence of a given piece.</p>
<h2 id="concepts-and-data">Concepts and Data</h2>
<p>We mainly focus ourselves on each song lyrics and its musical structure. The latter can be seen as repeated harmonic progressions, mainly in the form of sequences of chords, following the lyrics.<br>
As our core reference paper does, we will at first work with the Ultimate Guitar dataset which might be completed by using the Genius API to retrieve lyrics.<br>
After defining our measure of lyrical complexity  and musical complexity, we will observe their relationship and also their correlation with the intensity of the valence observed by a sentiment analysis on the lyrics.</p>
<p>In case we would like to go further, we think it could be interesting to study the full musical spectrum of each piece, instead of simply the chord progressions. By using MIDI files, we could analyse all the musical elements and study the link between complexity/valence and scales.<br>
We found an unsorted dataset of 130000 items <a href="https://www.reddit.com/r/datasets/comments/3akhxy/the_largest_midi_collection_on_the_internet/">here</a> that could be useful in that aim.</p>
<h2 id="methods">Methods</h2>
<p>In order to provide insight on the relationship between valence and complexity, we will use the work of Kolchinsky et al. as a starting point. Given the valence of songs, we will proceed to analyze the complexity of both lyrics and musical structure. The lexical complexity will be established based on syntax, sentence structure and vocabulary, using the methodology established by Suma Bhat and Su-Youn Yoon. For the musical structure, we will base ourselves on the paper written by Marsk et al.</p>
<h2 id="literature">Literature</h2>
<ul>
<li>Kolchinsky A, Dhande N, Park K, Ahn Y-Y. 2017 <a href="http://dx.doi.org/10.1098/rsos.170952">The Minor fall, the Major lift: inferring emotional valence of musical chords through lyrics.</a> R. Soc. open sci. 4: 170952.</li>
<li>Marsik L, Pokorny J, Ilcik M. 2014 <a href="https://pdfs.semanticscholar.org/c903/4270c01409df0da70d5266eb0868beda29a1.pdf">Towards a Harmonic Complexity of Musical</a></li>
<li>Suma Bhat, Su-Youn Yoon. 2014 <a href="https://ac.els-cdn.com/S0167639314000715/1-s2.0-S0167639314000715-main.pdf?_tid=f7f218cf-da04-45fb-b5c8-9bb96531e5a3&amp;acdnat=1521561519_a4db864919711cd42f236550c7204659">Automatic assessment of syntactic complexity for spontaneous speech scoring</a></li>
</ul>


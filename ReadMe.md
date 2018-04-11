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
<h4 id="data-gathering">Data Gathering</h4>
<ul>
<li>
<p><em><strong>How did you obtain/create it?</strong></em><br>
Web-scrapping from the ultimate guitar API was used to gather both the textual data and the chords from Ultimate Guitar.<br>
For the MIDI, it was a downloadable file that we directly took.</p>
</li>
<li>
<p><em><strong>In which format is the data?</strong></em>*<br>
Ultimate Guitar: text<br>
Unsorted MIDI: MIDI</p>
</li>
</ul>
<h4 id="preprocessing">Preprocessing</h4>
<ul>
<li>
<p><em><strong>Transform data so that you can effectively work with it.</strong></em></p>
</li>
<li>
<p><em><strong>Is there missing data that you need to account for?</strong></em></p>
</li>
<li>
<p><em><strong>Do you need to deal with biases in the data? How?</strong></em><br>
Because ultimate guitar is website for guitarists that is collaborative, it is essential to bear in mind that mostly pop-rock and easy to play songs will appear on the dataset. The same goes for the MIDI data. Since it is unsorted and coming from the internet, one must consider that the same collaborative way of working was applied. This means that the cultural bias and the oversimplicity problems are still an issue for the dataset.<br>
In order to treat those biases we must consider them in our research methodolgy. fine graining the analysis to what this data shows is important to avoid drawing inaccurate conclusions.</p>
</li>
</ul>
<h4 id="basic-statistics">Basic Statistics</h4>
<ul>
<li>
<p><em><strong>How are the features of the data distributed?</strong></em></p>
</li>
<li>
<p><em><strong>Can you identify correlations?</strong></em></p>
</li>
<li>
<p><em><strong>What can you already infer regarding your research question?</strong></em></p>
</li>
<li>
<p><em><strong>What are suitable visualizations for the initial results?</strong></em></p>
</li>
</ul>
<h4 id="subsequent-steps">Subsequent steps</h4>
<ul>
<li>
<p><em><strong>How will you proceed?</strong></em></p>
</li>
<li>
<p><em><strong>Do you need to adjust your research plan?</strong></em></p>
</li>
<li>
<p><em><strong>Which methods did you decide to use?</strong></em></p>
</li>
</ul>
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


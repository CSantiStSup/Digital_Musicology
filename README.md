# The relationship between complexity and emotion in music
By Santiago Saint Supéry and Pierre-Antoine Desplaces


## Research Question

Regardless of the quantification aspect, complexity in music is a central element. Music is constructed on a theoretical structure that allows many possibilities and variations, however many modern musical pieces are structured in a simple way. Apart from this aspect, music is a mean to share emotions, and because works have been done exploring both of those aspects, we intend to explore the link between them. In this project, we aim at linking complexity and emotion in music. Our goal is to find out if and how structural complexity in music writing in its broadest sense - that is to say for both instruments and lyrics - can have an impact on the emotional valence of a given piece.

## Concepts and Data

We mainly focus ourselves on each song lyrics and its musical structure. The latter can be seen as repeated harmonic progressions, mainly in the form of sequences of chords, following the lyrics.
As our core reference paper does, we will at first work with the Ultimate Guitar dataset which might be completed by using the Genius API to retrieve lyrics.
After defining our measure of lyrical complexity  and musical complexity, we will observe their relationship and also their correlation with the intensity of the valence observed by a sentiment analysis on the lyrics.

In case we would like to go further, we think it could be interesting to study the full musical spectrum of each piece, instead of simply the chord progressions. By using MIDI files, we could analyse all the musical elements and study the link between complexity/valence and scales.
We found an unsorted dataset of 130000 items [here](https://www.reddit.com/r/datasets/comments/3akhxy/the_largest_midi_collection_on_the_internet/) that could be useful in that aim.

## Methods

In order to provide insight on the relationship between valence and complexity, we will use the work of Kolchinsky et al. as a starting point. Given the valence of songs, we will proceed to analyze the complexity of both lyrics and musical structure. The lexical complexity will be established based on syntax, sentence structure and vocabulary, using the methodology established by Suma Bhat and Su-Youn Yoon. For the musical structure, we will base ourselves on the paper written by Marsk et al. 

## Literature
- Kolchinsky A, Dhande N, Park K, Ahn Y-Y. 2017 [The Minor fall, the Major lift: inferring emotional valence of musical chords through lyrics.](http://dx.doi.org/10.1098/rsos.170952) R. Soc. open sci. 4: 170952.
- Marsik L, Pokorny J, Ilcik M. 2014 [Towards a Harmonic Complexity of Musical](https://pdfs.semanticscholar.org/c903/4270c01409df0da70d5266eb0868beda29a1.pdf)
- Suma Bhat, Su-Youn Yoon. 2014 [Automatic assessment of syntactic complexity for spontaneous speech scoring](https://ac.els-cdn.com/S0167639314000715/1-s2.0-S0167639314000715-main.pdf?_tid=f7f218cf-da04-45fb-b5c8-9bb96531e5a3&acdnat=1521561519_a4db864919711cd42f236550c7204659)
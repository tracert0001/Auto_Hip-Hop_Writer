# Auto_LyricsWriter
Automatic English Hip-Hop Lyrics Writer

Hip-Hop/Rap is a modern form of poetry. Great rap lyrics are personal and flow like water, blending into the song while making a point or theme like a great essay or story might.
Like a burgeoning writer needs to study the best poets, a growing rapper needs to read to the great rappers for inspiration. However it seems that the ideas occur to the writer unpredictably and likely no correlation between them is guaranteed.   
Furthermore, it is hard for certain rappers to write lyrics with a variety of styles. To summarize, how to expand a few of ideas to a paragraph, find materials, and make words varied but coherent is the most challenging part of rap lyrics writing.

----

We built an automatic English Hip-Hop lyrics writer by using TensorFlow to create an LSTM (Long Short-Term Memory) neural network that reads all the Hip-Hop lyrics, it learned all the contexts, words, rhythms, etc. So now when it is given a prime word or phrase, it’ll generate a new lyric in Hip-Hop style. To gain more inspirations, we even train our model with Shakespeare‘s sonnet and poems, after which we can expand our prime words to more creative phrases and then try those out in the generator, see what will happen when Hip-Hop meets Shakespeare!

----

Demo:

![pic1](https://user-images.githubusercontent.com/89000685/143677162-0d9eaf9c-4502-4fe2-b0f2-3e6b2f605802.png)

![pic2](https://user-images.githubusercontent.com/89000685/143677157-bff29133-2759-4583-a9d8-0026bd8ba80d.png)

----

Dataset: 

* Hip-Hop Lyrics

** The number of Songs: 5384, most of them totally in English, but some contain a few Germany, Spanish or French words, which might also be regarded as a feature of Hip-Hop. (http://www.metrolyrics.com)

* Shakespeare’s Sonnet & Poem

** The number of Poems: 158, some of poems contain ancient English or other rare words. (http://shakespeare.mit.edu)

----

Our model is a sequence-to-sequence model, which reads in a sequence of length 5 and is given an initial state, then learns to output a sequence of the same length but ahead of the input sequence by one time step, so that it can capture the writing style. The model contains a 2-layer LSTM each with 256 units, got final model after 30000 steps training.

![pic3](https://user-images.githubusercontent.com/89000685/143677396-d8ccb550-e93c-4843-83c3-6455d17aa129.png)




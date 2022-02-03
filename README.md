# STSCI 4780/5780 Lecture Resources

In the reference lists below, references with "&sext;" are especially strongly recommended. *Kruschke* refers to John Kruschke's  [*Doing Bayesian Data Analysis* (2nd edition)](https://sites.google.com/site/doingbayesiandataanalysis/), one of the recommended texts for STSCI 4780. *Rethinking* refers to the other recommended text, McElreath's *Statistical Rethinking*. *BDA3* refers to the third edition of [*Bayesian Data Analysis*](http://www.stat.columbia.edu/~gelman/book/) by Gelman et al. (2013), the standard statistics-PhD-level reference on Bayesian data analysis.

## Lec01 - The big picture

Slides:  [Lec01-BigPicture.pdf](Lec01-BigPicture.pdf)

### Suggested reading

While not covering the Bayesian approach from a technical perspective, as we did in Lec01, Sharon McGrayne's 2012 book, [&sext; The Theory That Would Not Die](https://yalebooks.yale.edu/book/9780300188226/theory-would-not-die), provides a popular-level treatment of the history of Bayesian inference and its place in modern science. This book was a *New York Times* "Editor's Choice" selection; see the 2011 [pre-publication review](http://www.nytimes.com/2011/08/07/books/review/the-theory-that-would-not-die-by-sharon-bertsch-mcgrayne-book-review.html). For more info about the book, see [Sharon Bertsch McGrayne's "The Theory..." web page](http://www.mcgrayne.com/the_theory_that_would_not_die__how_bayes__rule_cracked_the_enigma_code__hunted_d_107493.htm). The book was timed to come out just before the 250th anniversary of the publication of Bayes's paper presenting a special case of what came to be called Bayes's theorem.  McGrayne was the dinner speaker at [Bayes 250 Day](https://web.archive.org/web/20161011035530/https://bayesian.org/meetings/Bayes250), a meeting held by the [International Society for Bayesian Analysis (ISBA)](https://bayesian.org/) in 2013 to honor the anniversary.

I can't resist a personal, astronomical note on the book. McGrayne interviewed me as part of her research for it. I get a brief mention (for helping to introduce Bayesian methods into modern astronomy). But our main correspondence and discussion was about Laplace's work, especially a famous calculation he did estimating the mass of Saturn. He used Bayes's theorem to estimate Saturn's mass from noisy data. His late-18th century parlance for what we today call a *credible region* went as follows:

> Applying to them my formulae of probability I find that it is a bet of 11,000 against one that the error of this result is not 1/100 of its value....

Indeed, today's best estimate is well within a percent of Laplace's estimate; he would have won that bet! See the forthcoming Lec02 notes for more from and about Laplace.

The main technical part of Lec01 concerned a key distinction between Bayesian and frequentist approaches: both approaches involve *computing averages and integrals*, but **over different spaces**. Bayesian probabilities typically involve sums or averages over the hypothesis or parameter space; frequentist probabilities instead sum or average over the data or sample space. Two papers of mine elaborate on this distinction (mainly in the early sections):

* [The Promise of Bayesian Inference for Astrophysics | SpringerLink](https://link.springer.com/chapter/10.1007/978-1-4613-9290-3_31) — An *old* (1991) paper using some simple examples to highlight this difference. For a longer version, see: [The Promise... (unabridged)](http://hosting.astro.cornell.edu/staff/loredo/bayes/promise.pdf).
* [Bayesian Astrostatistics: A Backward Look to the Future | SpringerLink](https://link.springer.com/chapter/10.1007/978-1-4614-3508-2_2) — This focuses more on concepts than calculations, and addresses some misunderstandings about the difference between Bayesian and frequentist approaches to quantifying uncertainty.

If you are very familiar with frequentist statistics, you may appreciate the following  paper by Ed Jaynes from the 1970s, when Bayesian methods were still considered controversial. It offers several example calculations displaying the difference results one can get when adopting Bayesian vs. frequentist approaches to simple problems; this paper inspired my 1991 paper cited above:

* [Confidence Intervals vs Bayesian Intervals | SpringerLink](https://link.springer.com/chapter/10.1007/978-94-010-1436-6_6) — Also available in a collection of some of Jaynes's most important papers ([E. T. Jaynes: Papers on Probability, Statistics and Statistical Physics | SpringerLink](https://link.springer.com/book/10.1007/978-94-009-6581-2)), and online as item 32 in the "E. T. Jaynes: Articles" section of [Probability Theory As Extended Logic - Bayesian resources at Washington U.](https://bayes.wustl.edu/)


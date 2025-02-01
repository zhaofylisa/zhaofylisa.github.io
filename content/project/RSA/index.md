---
title: 'Probabilistic Listener: A Case of Reflexive ziji "self" Ambiguity Resolution in Mandarin'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Brian Dillon
  - Ming Xiang


date: '2023-03-09T00:00:00Z'
# doi: ''

# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
# publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
Presentation: In *36th Annual Conference on Human Sentence Processing*
# publication_short: In *ICW*

# abstract: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum. Sed ac faucibus dolor, scelerisque sollicitudin nisi. Cras purus urna, suscipit quis sapien eu, pulvinar tempor diam. Quisque risus orci, mollis id ante sit amet, gravida egestas nisl. Sed ac tempus magna. Proin in dui enim. Donec condimentum, sem id dapibus fringilla, tellus enim condimentum arcu, nec volutpat est felis vel metus. Vestibulum sit amet erat at nulla eleifend gravida.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Psycholinguistics
  - Computational modeling

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: "uploads/RSA/RSA_pdf.pdf"
# url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_dataset: 'https://github.com/HugoBlox/hugo-blox-builder'
url_poster: "uploads/RSA/RSA_poster.pdf"
# url_project: ''
url_slides: "uploads/RSA/RSA_slides.pdf"
# url_source: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_video: 'https://youtube.com'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: Frank & Goodman (2012)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []
  # - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
### Probabilistic Listener: A Case of Reflexive ziji "self" Ambiguity Resolution in Mandarin
<sup> (This work was my honors thesis at UMass Amherst, and was advised by <a href = "https://www.umass.edu/linguistics/member/brian-dillon"> Dr. Brian Dillon </a> and <a href = "https://linguistics.uchicago.edu/people/ming-xiang"> Dr. Ming Xiang </a>.) </sup>
<br>
<sup> - <strong>Fengyue Zhao</strong>, Brian Dillon, Ming Xiang. Probabilistic Listener: A Case of Chinese Mandarin Reflexive ziji. Ambiguity Resolution. 36th Annual Conference on Human Sentence Processing. March 9 - 11 2023. University of Pittsburgh, Pittsburgh, PA. </sup>

What mechanisms do people use to resolve ambiguous pronouns? Prior studies have tried to identify factors that contribute to the resolution mechanisms, such as first-mention biases [1], verb semantics [2], and world knowledge[3]. These principles usually only make categorical predictions instead of continuous predictions about experimental data. Probabilistic models are another promising attempt [4][5][6][7]. This study aims to test the generality of two Bayesian models — the Simple Bayesian model (SBM) and the Rational Speech Act model (RSA) — on pronoun ambiguity resolution in Mandarin Chinese in the case of the reflexive pronoun ziji "self". SBM has been examined to make good quantitative predictions for Chinese, but only for across-sentence relations in discourses with personal pronouns [7]. RSA has been examined in pronoun resolution in French and English [6]. This study provides cross-linguistic evidence to support both Bayesian models, investigating within-sentence relations with Chinese reflexive pronouns which are often considered to be regulated by a distinct set of grammatical principles than discourse anaphors.

      (1)  [小红]i  说    [小明]j   总      把      [自己]i/j    弄糊涂。
          [Hong]i  says  [Ming]j always   BA     [ziji]i/j   confuses.
          ‘[Hong]i says that [Ming]j always confuses [self]i/j.’

**The resolution of reflexive ziji**: Reflexive in Mandarin may take a simplex form — ziji “self” which permits both local (e.g. Ming in 1) and non-local (e.g. Hong in 1) referent interpretation [8]. In Experiment 1 (Nsubj=135, Nitem=30), we measured Mandarin speakers’ preferences for resolving ziji in ambiguous sentences with an antecedent selection task. Stimuli have the sentence structure in (1), differing only in the verb. We found that comprehenders preferred local antecedents 59% of the time on average. This non-randomly distributed result showed that people have strategies to resolve this ambiguous reflexive. Moreover, the preference of non-local antecedents ranged between 9% and 88% across items. This non-uniform result showed that preferences and extent of preferences differ across stimuli items. Therefore, item-by-item quantitative analysis is necessary to test if two models can capture this item variation. 

![Formulars](/uploads/RSA/RSA_pic1.png)

**Two Bayesian Models**: The Simple Bayesian model (SBM) models the listener’s probability of selecting  a specific referent as proportional to their prior that this referent will be mentioned next, and the likelihood that a speaker will produce this pronoun when signaling a specific referent (see Formula 1) [5]. The Rational Speech Act model (RSA) suggests that listeners assume speakers are rational agents who have already chosen the best utterance among all possible options to convey intended information. Listeners combine this recursive thinking with their prior world knowledge to interpret ambiguous pronouns (see Formula 2) [4]. To evaluate these models’ fit against our data, we estimated: P(referent) in both models in Experiment 2, a world knowledge bias test (Nsubj=28, Nitem=30); P(utterance | referent) in SBM in Experiment 3, a pronoun production task (Nsubj=65, Nitem=30); Cost(utterance) in RSA in a corpus study (Ntoken=16.5 billion) which is the logarithm of the frequency of each pronoun in a certain sentence structure. If listeners processing ambiguous pronouns follows SBM/RSA, there should be a strong correlation between the Experiment 1 results and SBM/RSA predictions.

<figure>
<img src="/uploads/RSA/RSA_pic2.png" alt="Trulli" style="width:50%">
<img src="/uploads/RSA/RSA_pic3.png" alt="Trulli" style="width:50%">
<figcaption align = "center"><b>Fig.1 - Fit RSA model predictions (top) and SBM model predictions (bottom) with experimental data from Experiment 1 on an item-by-item basis.</b></figcaption>
</figure>

| | R-squared  | MSE | MAE   | P-value        |
| ------------ | ------------ | ------------ | -----------: | ------------------- |
|SBM| 0.598 | 0.025    | 0.138 | 0.0007|
|RSA| 0.674   | 0.006    | 0.048     |0.0002|

<p style ="text-align: center;"><b><span style="font-size:0.8em">Table 1. R-squared, MSE, MAE, and P-value of the two models for model evaluations.</span></b></p>


**Results and Discussions**: Item-by-item quantitative analysis in Fig.1 shows that both SBM and RSA can make accurate predictions for the resolution of the ambiguous pronoun ziji (R2>0.59, p<0.001), providing a case study to support that within-sentence reflexive binding obeys principles of Bayesian inference too. Meanwhile, although both SBM and RSA are Bayesian models, the statistical results in Table 1 show that RSA performs a little better while SBM overestimates the non-local antecedent choices and underestimates the local antecedent choices. The difference between two models is that listeners in SBM reason about the production of the pronoun directly using their own experience without encoding explicit the frequency of pronouns, while listeners in RSA are rational and reason indirectly by thinking about how a rational speaker would choose pronouns, and this rational speaker would explicitly take the frequency of pronouns into account (the Cost term in Formula 2). One possible explanation for this is that a multilevel recursive reasoning between listeners and speakers coupled with the explicitly encoded frequency of pronouns could enhance model predictions, leading to a better fit between RSA and the experimental data. 

### References
[1] Järvikivi, J., van Gompel, R. P., Hyönä, J., & Bertram, R. (2005). Psychological Science. 

[2] Koornneef A. W., & van Berkum J. J. A. (2006). Journal of Memory and Language. 

[3] Hobbs, J. R. (1979). Cognitive Science.   

[4] Frank, M. C., & Goodman, N. D. (2012). Science.      

[5] Kehler, A, & Rohde, H. (2013). Theoretical Linguistics. 

[6] Schulz, M., Burnett, H., & Hemforth, B. (2021). A Journal of General Linguistics. 

[7] Zhan, M., Levy, R., Kehler, A. (2020). PLOS ONE. 

[8] Huang, C.-T. J., Li, Y.-h. A., & Li, Y. (2009). Cambridge University Press. 


---
title: 'Syllable Position Prominence in Unsupervised Neural Network Segment Categorization'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Sam Tilsen

share: false
date: '2024-03-30T00:00:00Z'
# doi: ''

# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
# publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *LabPhon 19*
# publication_short: In *ICW*

# abstract: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum. Sed ac faucibus dolor, scelerisque sollicitudin nisi. Cras purus urna, suscipit quis sapien eu, pulvinar tempor diam. Quisque risus orci, mollis id ante sit amet, gravida egestas nisl. Sed ac tempus magna. Proin in dui enim. Donec condimentum, sem id dapibus fringilla, tellus enim condimentum arcu, nec volutpat est felis vel metus. Vestibulum sit amet erat at nulla eleifend gravida.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Unsupervised learning
  - Phonological categories
  - Computational modeling
  

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: "uploads/NN/NN.pdf"
# url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_dataset: 'https://github.com/HugoBlox/hugo-blox-builder'
url_poster: "uploads/NN/NN_poster.pdf"
# url_project: ''
# url_slides: ''
# url_source: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_video: 'https://youtube.com'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  # caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
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

<sup> - <strong>Fengyue Zhao</strong>, Sam Tilsen. Syllable Position Prominence in Unsupervised Neural Network Segment Categorization. LabPhon 19. June 27 - 29 2024. Hanyang University, Seoul, South Korea. </sup>

## Motivation
English obstruents exhibit diverse phonetic realizations across syllable positions, like /t/ and /p/ in words such as top and pot [1]. Linguistically we assume that phone identity—(e.g. /p/ vs. /t/) is a strong predictor of representational similarity, while syllable position—e.g. onset vs. coda—is perhaps a secondary factor. But is this always the case? Unsupervised learning in neural networks presents a practical approach for exploring this interplay, because it does not require presuppositions about phonological categories such as segments and syllable. Previous studies [2, 3] have demonstrated the capacity of neural networks to learn abstract representations from acoustic signals. This study employed an unsupervised autoencoder neural network to explore the correlation between phonological categories and network-learned representations. Surprisingly, we found that for consonants, syllable position plays a larger role in representational similarity than phone identity.

## Method
<u> Data</u>: In order to enhance the interpretability of neural models, we chose to use a controlled experimental dataset to investigate the interplay between syllable position and segment identity. The dataset comprised nine syllables corresponding to all combinations of {p, t, Ø}onset × /a/ ×{p, t, Ø}coda (note that onset Ø was realized as glottal stop [ʔ]), with /p/ and /t/ appearing in onset position (denoted as p1 and t1) and coda position (p2 and t2). Examples included [p1at2], [ʔap2], etc. The syllables were articulated following an initial prolonged [i]. <u>Model</u>: The autoencoder architecture [2] (see Fig. 1a) encompassed an encoder compressing acoustic input into a latent representation (labeled R) and a decoder reconstructing the input. The inputs were 12-coefficient MFCC vectors (window: 25ms hamming, hop time: 1ms, range: 0 - 8000 Hz). Notably, the autoencoder acquired a compact representation of the input in the latent representation R, without utilizing explicit labeling during training. The data were divided into training (60%), validation (20%), and test sets (20%). <u>Analysis</u>: During testing, all 7 individual categories (i.e., aa, iy, ʔ, p1, t1, p2, t2) were fed into the autoencoder model. Subsequently, extracted latent representations (patterns of node activation in R) were subjected to dimensionality reduction via t-SNE (t-distributed Stochastic Neighbor Embedding), followed by K-means clustering to assess activation pattern similarities within the R space  (Fig. 1b).

<figure>
  <img src="/uploads/NN/method.png"/>
  <figcaption>Figure 1. (a) Model: an autoencoder architecture. (b) Analysis: the analysis prosedure.</figcaption>
</figure>


## Results
For consonants, syllable position emerged as a stronger predictor of representational similarity than segment identity. In Fig. 2a, consonants sharing the same syllable position but different identities (e.g. onset p1, t1, ʔ) were closer to each other in the representation space compared to consonants of the same identity in different positions (e.g. onset p1 and coda p2). This observation was further supported by the k-means clustering result. Fig. 2a shows the locations of individual segment tokens in representational space, along with grey convex hulls surrounding clusters. With k=4 clusters, k-means algorithm effectively separated the two vowels [i] and [a], while also forming clusters of onset sounds (p1, t1, and ʔ) and coda sounds (p2, t2). Certain instances of glottal stops [ʔ] were grouped with [i]’s, potentially explained by varied phonetic realizations — some as full glottal plosives while others may exhibit creakiness. Sub-clusters for [i] and [a] were associated with individual speakers. The k=4 clustering achieved strong performance metrics (V-Measure: 0.78, Completeness: 0.90, Homogeneity: 0.69) compared to other values of k. Fig. 2b shows that increasing the cluster count does not lead to distinct clusters associated with segment identity. The V-measure score, a harmonic mean between completeness and homogeneity, was in fact maximal for k=4, suggesting that separating onsets and codas provides the optimal clustering of sound categories.


<figure>
  <img src="/uploads/NN/results2.png"/>
  <figcaption> <p align='left'>Figure 2. (a) K-means clustering result when k=4. This illustration shows the locations of individual segment tokens in representational space R, along with grey convex hulls surrounding clusters. The boxed annotations summarize the 4 clusters: [i]’s, [a]’s, onsets, and codas. (b) Evaluation metrics (V-Measure, Completeness, Homogeneity) of k-means clustering across k values (2 to 10), illustrating performance fluctuations with cluster count. </p> </figcaption>
</figure>


## Conclusion
Our results show that syllable position is more influential than segment identity in representational space learned by the neural network from acoustic signals. This is important because it suggests that the role of syllable position in human representations may be underappreciated. Future exploration of this finding with larger datasets will be of value.

## References
[1] Turk, A. (1994). Phonological Structure and Phonetic Form: Articulatory phonetic clues to syllable affiliation: gestural characteristics of bilabial stops. 

[2] Shain, C., & Elsner, M. (2019). Measuring the perceptual availability of phonological features during language acquisition using unsupervised binary stochastic autoencoders. Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, 69–85. 

[3] Shain, C., & Elsner, M. (2020). Acquiring language from speech by learning to remember and predict. Proceedings of the 24th Conference on Computational Natural Language Learning, 195–214.

---
title: 'Laryngeal Elevation in Native and Non-native Lexical Tone Production'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Sam Tilsen
  - Mark Tiede

share: false
date: '2026-05-04T00:00:00Z'
# doi: ''

# Schedule page publish date (NOT publication's date).
# publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
# publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *LabPhon 20* & *ASA*
# publication_short: In *ICW*

# abstract: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum. Sed ac faucibus dolor, scelerisque sollicitudin nisi. Cras purus urna, suscipit quis sapien eu, pulvinar tempor diam. Quisque risus orci, mollis id ante sit amet, gravida egestas nisl. Sed ac tempus magna. Proin in dui enim. Donec condimentum, sem id dapibus fringilla, tellus enim condimentum arcu, nec volutpat est felis vel metus. Vestibulum sit amet erat at nulla eleifend gravida.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Tones
  - Ultrasound imaging
  

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: "uploads/ultrasoundTones/abstract.pdf"
# url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_dataset: 'https://github.com/HugoBlox/hugo-blox-builder'
url_poster: "uploads/ultrasoundTones/poster.pdf"
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

<sup> - <strong>Fengyue Lisa Zhao</strong>, Sam Tilsen, & Mark Tiede. Laryngeal elevation in native and non-native lexical tone production. 190th Meeting of the Acoustical Society of America. May 11 – 15, 2026. Philadelphia, PA, USA. </sup>

<sup> - <strong>Fengyue Lisa Zhao</strong>, Sam Tilsen, & Mark Tiede. Laryngeal elevation in native and non-native lexical tone production. LabPhon 20. June 26 – 28, 2026. Montréal, Québec, Canada. </sup>


## Motivation
Prior acoustic studies have found differences between native and non-native speakers in precision of lexical tone production, but corresponding differences in articulatory mechanisms remain underexplored. This study presents a novel comparison of laryngeal elevation in native and non-native speakers during tone production using coronal-orientation laryngeal ultrasound. Both laryngeal elevation and cricothyroid contraction can contribute to vocal fold tension and thus f0 modulation [1, 2], yet their relative roles have been difficult to assess, mostly due to methodological challenges. We hypothesized that native and non-native speakers differ in their reliance on extrinsic (laryngeal elevation) versus intrinsic (cricothyroid) mechanisms of f0 control to produce tone contrasts, with native speakers relying more on intrinsic control and non-native speakers more on extrinsic control. This predicts weaker correlations between laryngeal elevation and f0 in native speakers than in non-native speakers. Our results support this prediction and suggest a broader acquisition pattern: learning to produce tones may involve reweighting articulatory strategies, shifting from general extrinsic mechanisms toward intrinsic control.

## Method
Four participants were tested: two speakers of languages without lexical tone and two native Mandarin speakers. The non-native speakers were phonetically trained and produced Mandarin tones on the basis of standard numeral representations. The ultrasound probe was held by the participant at the right thyroid lamina in a coronal orientation to capture vertical laryngeal movement, following the protocol in [1, 3, 4]. Synchronized audio and laryngeal ultrasound (with a standard clinical convex probe, 90-100 fps) were recorded simultaneously. All participants completed blocks of high-to-low (HL) and low-to-high (LH) pitch sweeps along with repetitions of four Mandarin tones in the syllable ma. Two approaches were used to infer laryngeal elevation from ultrasound images: (i) image pixel intensity centroid, and (ii) weighted sum of pixel intensity sampled on a semipolar image grid, with weights from averages of lasso regressions predicting f0.  Figure 1 shows representative frames from an HL sweep, along with f0 and intensity centroid, confirming that changes in intensity centroid values reflect f0 movement in sweeps. Figure 2 shows example f0 trajectories and laryngeal-elevation traces from the lasso-based method for one native and one non-native male speaker. The lasso-based method was found to effectively identify image regions most predictive of f0, reducing noise from irrelevant portions of the ultrasound field.

<figure>
  <img src="/uploads/ultrasoundTones/method.png"/>
  <figcaption>Figure 1. Two laryngeal ultrasound frames an HL pitch sweep. Changes in intensity centroid values (red) reflect f0 movement (black).</figcaption>
</figure>

<figure>
  <img src="/uploads/ultrasoundTones/method2.png"/>
  <figcaption>Figure 2. Example f0 trajectories and elevation index values from lasso-based method for a native (S03) and a non-native (S04) speaker. Horizontal bars at the top show durational differences between tones.</figcaption>
</figure>


## Results
Preliminary analyses with both measures replicate the general pattern reported in [1]: larynx elevation is positively correlated with f0 across tasks. Figure 3a presents correlation coefficients between the centroid-based laryngeal elevation measure and f0 for each participant. The two female speakers showed higher correlations than the two male speakers, a pattern opposite to that reported in [1]. Crucially, Figure 3b compares correlations between sweeps and tones. Native speakers show stronger correlations between laryngeal elevation and f0 in sweeps than in tones, whereas non-native speakers show either weaker or the opposite effect. Under the assumption that the elevation-f0 correlation for sweeps provides a reference value for utilization of laryngeal elevation, the greater reduction in correlation from sweeps to tones observed in native vs. non-native speakers indicates that in the course of learning native speakers of tone languages may come to rely less on extrinsic laryngeal elevation and more on intrinsic muscle activity (e.g., cricothyroid manipulation) to produce tones than their non-native counterparts. Overall, these findings support a role for laryngeal elevation in tone production, while also motivating a broader hypothesis: speech learning may involve a shift in synergistic organization across articulatory mechanisms. This hypothesis can be tested in future work with larger samples.

<figure>
  <img src="/uploads/ultrasoundTones/result.png"/>
  <figcaption>Figure 3. (a) Correlation between laryngeal elevation (centroid-based) and f0 for each participant across sweeps and tones. 
  (b) Difference in correlations between sweeps and tones; positive values indicate a greater correlation in weeps than in tones.
  </figcaption>
</figure>


## References
[1] Moisik, S. R., Lin, H., & Esling, J. H. (2014). A study of laryngeal gestures in Mandarin citation tones using simultaneous laryngoscopy and laryngeal ultrasound (SLLUS). 

[2] Honda, K., Hirai, H., Masaki, S., & Shimada, Y. (1999). Role of Vertical Larynx Movement and Cervical Lordosis in F0 Control. 

[3] Brunelle, M., Schweizer, D., & Ahn, S. (2025). An ultrasound study of the role of larynx height and tongue movement in the production of Javanese registers.

[4] Schweizer, D., Brunelle, M., Ahn, S., & Audet, A. (2025). A laryngeal and lingual ultrasound study of the Canadian French voicing contrast.


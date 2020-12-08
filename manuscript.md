---
author-meta:
- Hossein Kabir
bibliography:
- content/manual-references.json
date-meta: '2020-12-08'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Pore in Concrete-Group8" />

  <meta name="citation_title" content="Pore in Concrete-Group8" />

  <meta property="og:title" content="Pore in Concrete-Group8" />

  <meta property="twitter:title" content="Pore in Concrete-Group8" />

  <meta name="dc.date" content="2020-12-08" />

  <meta name="citation_publication_date" content="2020-12-08" />

  <meta name="dc.language" content="en-US" />

  <meta name="citation_language" content="en-US" />

  <meta name="dc.relation.ispartof" content="Manubot" />

  <meta name="dc.publisher" content="Manubot" />

  <meta name="citation_journal_title" content="Manubot" />

  <meta name="citation_technical_report_institution" content="Manubot" />

  <meta name="citation_author" content="Hossein Kabir" />

  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />

  <meta name="citation_author_orcid" content="0000-0002-2222-6188" />

  <link rel="canonical" href="https://hosseinkabiruiuc.github.io/group8/" />

  <meta property="og:url" content="https://hosseinkabiruiuc.github.io/group8/" />

  <meta property="twitter:url" content="https://hosseinkabiruiuc.github.io/group8/" />

  <meta name="citation_fulltext_html_url" content="https://hosseinkabiruiuc.github.io/group8/" />

  <meta name="citation_pdf_url" content="https://hosseinkabiruiuc.github.io/group8/manuscript.pdf" />

  <link rel="alternate" type="application/pdf" href="https://hosseinkabiruiuc.github.io/group8/manuscript.pdf" />

  <link rel="alternate" type="text/html" href="https://hosseinkabiruiuc.github.io/group8/v/372a1ab667bedec070de1c2b1159b9cc2fd697ab/" />

  <meta name="manubot_html_url_versioned" content="https://hosseinkabiruiuc.github.io/group8/v/372a1ab667bedec070de1c2b1159b9cc2fd697ab/" />

  <meta name="manubot_pdf_url_versioned" content="https://hosseinkabiruiuc.github.io/group8/v/372a1ab667bedec070de1c2b1159b9cc2fd697ab/manuscript.pdf" />

  <meta property="og:type" content="article" />

  <meta property="twitter:card" content="summary_large_image" />

  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />

  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />

  <meta name="theme-color" content="#ad1457" />

  <!-- end Manubot generated metadata -->'
keywords: null
lang: en-US
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: Pore in Concrete-Group8
...






<small><em>
This manuscript
([permalink](https://hosseinkabiruiuc.github.io/group8/v/372a1ab667bedec070de1c2b1159b9cc2fd697ab/))
was automatically generated
from [hosseinkabiruiuc/group8@372a1ab](https://github.com/hosseinkabiruiuc/group8/tree/372a1ab667bedec070de1c2b1159b9cc2fd697ab)
on December 8, 2020.
</em></small>

## Authors



+ **Hossein Kabir**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0002-2222-6188](https://orcid.org/0000-0002-2222-6188)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [hosseinkabiruiuc](https://github.com/hosseinkabiruiuc)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>



# CEE 498 Project: Characterization of Porosity in Cement Paste Matrix


Faisal Qadri, PhD Student, Construction Materials Group, University of Illinois
Hossein Kabir, PhD Student, Construction Materials Group, University of Illinois
Tianshu Xiao, MS Student, Construction Management, University of Illinois


## Abstract

This research investigates applicability of image-based analysis to quantify and classify porosities in grayscale scanning electron microscopy (SEM) images, made from polished thin section of hydrated cement beams. Within the past decades, mercury intrusion porosimeter (MIP) technique has been used to measure pore volume fraction in cement-based matrices. However, MIP method was found to overestimate porosity as it is incapable of quantifying disconnected pores. Therefore, it is of interest to determine whether image analysis coupled with Artificial Neural Network (ANN) or Convolutional Neural Network (CNN) could characterize porosity. Accordingly, images pre-analyzed by ImageJ commercial software are used to calibrate the python code. The calibrated model was used for Exploratory Data Analysis (EDA) for feature engineering. The extracted features, which are likely to be predictive of porosity, are used to train the employed machine learning models. Results of the present study revealed the applicability of ANN for estimating porosity based on physical properties of pores and chemistry of hydrates. Also, CNN is found to be an efficient way of classifying SEM images having different pore volume fraction. The present research has the potential to be used in future to predict the remaining service life and the physicochemical properties of the cement matrix.

#### Keywords: 
Scanning Electron Microscopy (SEM), Mercury Intrusion Porosimeter (MIP), Artificial Neural Network (ANN), Convolutional Neural Network (CNN), Exploratory Data Analysis (EDA), porosity



# Introduction

 Durability of concrete structures against gradual ingress of deleterious liquids is mainly controlled by porosity and pore structure of cement paste matrix [1]. Pore structure is mainly divided into two main categories: capillary and gel pores and they range from few millimeters into few nano-meters having 70-90% of total porosity in the nano scale. There are multiple factors that affect general properties of capillary pore structure in concrete, which include curing regimes, cementitious materials contents, and water-to-cementitious materials ratios [1-2]. Therefore, it is necessary to precisely measure and characterize pore structure in concrete to determine the optimum concrete curing conditions and mix proportions. 
 
 Over the past few decades, mercury intrusion porosimeter (MIP) test has been used to measure porosity and pore size distribution in cement-based composites. In this method, using relatively high pressure, mercury is injected into the pore spaces of the matrix to determine porosity and its structure. MIP test, with an ability to measure pore sizes in the range of 0.006–500 µm, is typically performed on a small oven-dried cement-composite specimen and mercury is gradually applied on the desired surface [1]. However, it has been reported that, cement matrix surface tension as well as mercury contact angle with cement pore wall affects the accuracy of MIP measurements [3]. Moreover, MIP needs speciemn preparation; it is hard to conduct; and it is deemed a destructive test in such it damages weak microstructure due to the applied high pressure.

To address the uncertainty of MIP results, image analysis method is recently developed to directly measure paste matrix porosity. Backscattered scanning electron microscopy (SEM) images of polished impregnated epoxy concrete surface is captured and analyzed using ImageJ commercial software [1]. To go further, ImageJ software quantifies the total area of pores using a grayscale thresholded image. However, this commercial software solely provides total porosity of the matrix and lacks the ability to characterize porosity [1]. In addition, comparing the total porosity of paste matrices measured by MIP method with that measured by ImageJ revealed that porosity is underestimated in the former technique. In fact, in contrary to MIP, Image analysis is capable of measuring both connected and disconnected capillary pores, and hence gives a more realistic picture of the paste matrix pore system [1]. Also, SEM technique is easy to conduct since it does not need and specimen preparation, but costs a lot of money.

As a result, it is required to develop an image analysis-based technique to not only determine total porosity, but also characterize the pore structure, such as shape, size, and angularity of the pore system. For this reason, robust codes are written in python to read and analyze greyscale thresholded 200 SEM images. The present analysis is calibrated by matching average porosity found by python-based image analysis with that of ImageJ software. The calibrated model is then used to read images to find pore size distribution of the matrix. In the next step, chemistry of hydrates and angularity of pores are estimated to be used as features for the employed machine learning algorithms. Results of the present analysis revealed that ANN is a robust technique being capable of correlating pore volume fraction with angularity of pores, as well as chemistry of hydrates. In addition, porosities are classified into different categories using an optimized CNN. The relatively low Root Mean Squared Error (RSME) values of the two machine learning techniques, i.e. ANN and CNN, proposes the robustness of the present methodology over MIP for characterizing porosity in cement paste matrix. 


## References

[1] Nedunuri, S. S. S. A., Sertse, S. G., & Muhammad, S. (2020). Microstructural study of Portland cement partially replaced with fly ash, ground granulated blast furnace slag and silica fume as determined by pozzolanic activity. Construction and Building Materials, 238, 117561.
[https://doi.org/10.1016/j.conbuildmat.2019.117561](https://doi.org/10.1016/j.conbuildmat.2019.117561)

[2] Li, L., Wang, R., & Zhang, S. (2019). Effect of curing temperature and relative humidity on the hydrates and porosity of calcium sulfoaluminate cement. Construction and Building Materials, 213, 627-636.
[https://doi.org/10.1016/j.conbuildmat.2019.04.044](https://doi.org/10.1016/j.conbuildmat.2019.04.044)

[3] He, Z., Cai, R., Chen, E., & Tang, S. (2019). The investigation of early hydration and pore structure for limestone powder wastes blended cement pastes. Construction and Building Materials, 229, 116923.
[https://doi.org/10.1016/j.conbuildmat.2019.116923](https://doi.org/10.1016/j.conbuildmat.2019.116923)

[4] Hu, C., & Li, Z. (2014). Micromechanical investigation of Portland cement paste. Construction and Building Materials, 71, 44-52. [https://doi.org/10.1016/j.conbuildmat.2014.08.017](https://doi.org/10.1016/j.conbuildmat.2014.08.017)

[5] Takashimizu, Y., & Iiyoshi, M. (2016). New parameter of roundness R: circularity corrected by aspect ratio. Progress in Earth and Planetary Science, 3(1), 2.
[DOI 10.1186/s40645-015-0078-x](https://link.springer.com/article/10.1186/s40645-015-0078-x) 




<div id="refs"></div>

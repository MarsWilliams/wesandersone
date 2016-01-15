# Course Project
WESANDERSONE
A sone is a subjective unit of measure to describe loudness. A wesandersone is a subjective unit of measure to describe the loudness at which an image screams, 'Wes Anderson!'

## Overview

Wes Anderson's films are lauded by designers for his color composition and graphic styling. For my project, I will analyze stills from Anderson's films, extracting information about hue, saturation, and value.

My objective is to create a color template that describes Wes Anderson's visual aesthetic.
I want to use this template to create an image filter that will wesandersonify any submitted image.

## Methodology
1. Create a script to upload Wes Anderson film stills to Kuler, and use Kuler to generate five color palettes per image.
2. Follow the methodology outlined in the paper Color Compatibility From Large Datasets.
  a. Create a feature vector from color spaces, as defined by the total Kuler dataset: the five colors themselves, colors sorted by lightness, differences between adjacent colors,   sorted color differences, mean, standard deviation, median, max, min, and max minus min across a single channel
  b. Create scores for the Wes Anderson color palettes, examining the percentage of colors in each hue, the percentage of adjacent colors, and the percentage of colors in the same theme.
3. Use K-Means Nearest Neighbors for naiive clustering and exploration
4. Use LASSO to develop a linear model describing Kuler color palette wesandersone rating

## Deliverables
* Jupyter notebook documenting data exploration
* Jupyter notebook documenting feature analysis
* Jupyter notebook documenting modeling
* Research paper describing work
* Presentation distilling research
* Web interface for wesandersone with the following features:
  * image upload
  * raw image wesandersone rating
  * raw image analysis plots
  * image filter button
  * filtered image analysis plots to describe transformation
  * image share capabilities

## Dataset
The datasets I will use are available online, and are free to download.
* Film stills (raw images)  
http://film-grab.com/category/wes-anderson/
* Kuler/Colourlovers palette dataset (matlab data files)  
http://www.dgp.toronto.edu/~donovan/color/

## Tools
I will leverage the open sources Python modules OpenCV-Python and Scikit-Image to analyze the histograms of the stills.
* Open-CV-Python  
https://opencv-python-tutroals.readthedocs.org/en/latest/
* Scikit-Image  
http://scikit-image.org/docs/stable/api/api.html
* colorsys  
https://docs.python.org/2/library/colorsys.html

## Resources
#### Journal Articles
* Peter O'Donovan, Aseem Agarwala, Aaron Hertzmann. Color Compatibility From Large Datasets. ACM Transactions on Graphics, 2011, 30, 43, (Proc. SIGGRAPH).  
http://www.dgp.toronto.edu/~donovan/color/colorcomp.pdf
* S. Xue, A. Agarwala, J. Dorsey, H. Rushmeier / Learning and Applying Color Styles From Feature Films  
http://graphics.cs.yale.edu/su/pub/PG13/FilmStyle_1_Submit.pdf
* ImageNet Classification with Deep Convolutional Neural Networks  
http://www.cs.toronto.edu/~fritz/absps/imagenet.pdf

#### Tutorials
* Python for Image Manipulation  
http://www.cs.uregina.ca/Links/class-info/325/PythonPictures/
* Uploading files with Selenium  
https://muthutechno.wordpress.com/2014/07/09/uploading-files-in-selenium-webdriver/
* Deep Learning  
http://www.deeplearning.net/tutorial/lenet.html#lenet

#### Blogs
* Wes Anderson color palettes  
http://wesandersonpalettes.tumblr.com/

## To Do
### Pre-Analysis
<s>* Download datasets</s>
* Load colorCode data in database
* Write Kuler web browser script
* Load Wes Anderson theme palettes in database

### Exploration
* Explore dataset using numpy, pandas, sckikit-image, and open-cv-python

### Analysis
* Develop feature vector for theme palettes

### Modeling
* Create KNN model
* Create LASSO model
* Create hierarchical clustering model

### Paper
* Create Outline
* First draft
* Edit first draft
* Second draft
* Edit second draft
* Final draft

### Presentation
Create slides.js presentation distilling work

### Website Development
* Create image upload feature
* Create image rating display
* Create image plot display
* Create filter button
* Create filter plot display
* Incorporate social media share widgets

# GSERM_Text_Remote_admin
GSERM Text Mining Course for Remote Participation

**Each day, please perform a `git pull` to get the most up to date files and lessons.**

## Lesson Structure
Each day's lesson is contained in the [lesson](www.github.com/kwartler/) folder.  Each individual lesson folder will contain the following files and folders.

* Markdown (`.rmd`) & HTML - lays out learning objectives, commentary if applicable, data files, R scripts and slides used in the *entire* lesson.  Also has a link to the recording.  
* `recordedLesson` folder 
  * `data` sub folder- contains the data to be analyzed in the recorded session
  * `scripts` - the scripts that are covered in the recorded slide presentation.  Most students like to follow along running code as I explain and run it rather than merely watching themselves.
  * slides - A copy of the presentation covered in the recording.  Some students print the slides and begin to take notes.
* `labSession` folder 
  * `data` sub folder - contains the data we will work through together
  * `scripts` - scaffolded scripts to start our lab session

## Environment Setup
* The University is providing virtual machines for participants to run R code and perform analysis.  They will be providing that information to you and supporting any technical issues.

* As a backup, a student *could* use  [https://rstudio.cloud](https://rstudio.cloud). 
  * If using this method, please follow the setup instructions [here](https://github.com/kwartler/GSERM_TextMining/blob/master/Rstudio_Cloud_Instructions.docx) to set up a cloud space for programming & connecting to git.  Since you are just setting up, you will need to click "download" from the link to get the word doc directly.  After that files can be delivered through a `git pull`.

* You *can* install R, R-Studio & Git locally on your laptop but any system issues will be yours to resolve.  

- If you encounter any errors during set up don't worry!  Please request technical help from Prof K and the university.  The `qdap` library is usually the trickiest because it requires Java and `rJava`.  So if you get any errors, try removing that from the code below and rerunning.  This will take **a long time**, so if possible please run prior to class, and at a time you don't need your computer ie *at night*.  We will work to resolve any issues prior to class or during Monday's live session.

## R Packages

```
# Easiest Method to run in your console
install.packages('pacman')
pacman::p_load(ggplot2, ggthemes, stringi, hunspell, qdap, spelling, tm, dendextend,
wordcloud, RColorBrewer, wordcloud2, pbapply, plotrix, ggalt, tidytext, textdata, dplyr, radarchart, 
lda, LDAvis, treemap, clue, cluster, fst, skmeans, kmed, text2vec, caret, glmnet, pROC, textcat, 
xml2, stringr, rvest, twitteR, jsonlite, docxtractr, readxl, udpipe, reshape2, openNLP, vtreat, e1071)

# Additionally we will need this package from a different repo
install.packages('openNLPmodels.en', repo= 'http://datacube.wu.ac.at/')

# You can install packages individually such as below if pacman fails.
install.packages('tm')

# Or using base functions use a nested `c()`
install.packages(c("lda", "LDAvis", "treemap"))

```

## Prerequisite Work
*  Read chapter 1 of the book [Text Mining in Practice with R](https://www.amazon.com/Text-Mining-Practice-Ted-Kwartler/dp/1119282012) book.

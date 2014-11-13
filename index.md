---
title       : Cheight-predict App Pitch
subtitle    : Predicting your child's adult height
author      : Kevin Low
job         : Data Products Course Student
framework   : io2012         # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introducing Cheight-predict

# What It Does?
1. Provides a prediction of your child's height based on yours (& perhaps also that of your partner's)
2. Maps your child's predicted height on the distribution of heights in the dataset used for the prediction model



# General Features

1. Simple to use, intuitive user interface
2. Reactive Output utilizing Shiny's engine
3. Runs right off your browser!

---

## Input Features

1. Flexibility of selecting prediction models (user as the father or mother; both parents heights included or just one)
2. Model accounts for child's gender
3. Input in 'inches' or 'centimeters' accepted

---


## Output Features

1. Child's predicted height in 'inches' and 'centimeters'
2. Shows child's height positioning on the distribution of heights in the dataset
3. Completely reactive, without submit button

Note however that the output contains an error message when none of the parents are selected for the model input.

---

## Sample Output

Backend model function generates the *cheight* variable which is presented to users in both inches and centimeters.


```r
cheight <- modsel(input$pheight, input$fheight, input$mheight, input$cgender)
```

Say, we have a predicted height of 67.221 inches for a boy; the app also generates the following charts:

![plot of chunk samdist](assets/fig/samdist.png) 


---

## Afterthoughts

Cheight-predict available right now on a [Shinyapps.io page](http://kevinlxk.shinyapps.io/heightpredict).

Open-source: UI and Backend codes are available on my [github page](https://github.com/kevinlxk/heightpredict).

You are very welcomed to develop this app with me, further enhancing functionality and accounting for more variables or improving the prediction algorithm.


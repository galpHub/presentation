---
title       : Reproducible pitch presentation
subtitle    : A simple data product for species identification
author      : Germán Luna
job         : Getones Inc.
logo        :
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Summary

Using random forests to predict species of Iris plants https://galphub.shinyapps.io/ShinyApp.

### Features

1. Requires 4 parameters corresponding to quantitative plant features (i.e. sepal length, sepal width, petal length and petal width) as input.
2. The inputs will be displayed reactively on the main panel (to the right). 
3. The predicted value of species will only appear after hitting the predict button.
4. If a mistake is made as to the chosen values of the inputs, or one wishes to reset the values to their default, clicking the "Reset inputs" button will reset the parameter values to their median value (i.e. their initial values).

--- .nobackground #foo

## Additional features (cont.)
5. A plot of two of the variables in the data set are provided to guide the user in choosing some test values for the app.
6. Some features of the plot are reactive to slider inputs. 
 * The top slider, petal length, controls the size of the points. It enlarges (resp. shrinks) points of species X as the parameter values approaces (resp. moves away from) the median of petal length for that species.
 * Petal width and sepal length control the black lines on the plot.


<script>
$("#foo ol").attr('start', 5)
</script>

---

## Final comments about prediction algorithms via apps.

Developing apps can be a difficult task depending on the machine learning task at hand.One must balance interactivity and visualization with accuracy. A task may be so involved that for most parameter settings an algorithm will predict similar or identical values. Consequently visualizations have to be incorporated to help the user understand how the data and the model interact. Ommiting such visualizations may give the impression that the fancy application is just predicting the mean value and consequently not very reliable.

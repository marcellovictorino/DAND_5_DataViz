# From Data Visualization to Story Telling
Data visualization projects covered in Udacity's Data Analyst Nanodegree (Module 5).

Data Visualization is a critical skill for Data Science, since it doesn't matter if you have the most accurate predictive model or the most valuable business insight if you are not able to communicate their value and convince others to use it.

Basically, it can be divided into 2 stages:

1. **Exploration**: while performing EDA, getting better intuition about the data you are working on, these visualizations are mainly to support/complement your own understanding. Therefore, they don't have to be perfectly finished - a quick prototyping is more relevant at this point.
2. **Explanatory**: after completing the analysis, helps to communicate your main findings and conclusions to others, even for non-technical audience, including a Call to Action on what to do after having this new information. At this point, you need to focus on low *chart junk*, high *data/ink ratio*, choosing the appropriate *encodings*, making sure the visual element convey indeed the desired message.

> *"Strive for Elegance and Simplicity"*

## Design of Visualizations

Keep in mind the data type to choose the best encodings and forms to visualize them.

**Qualitative**:

 - Nominal: labels without order (categories, locations)
 - Ordinal: labels whit meaningful ordering (ranking, rating, Likert scale)

**Quantitative**:

 - Discrete:
 - Continuous:

## Bad Viz

Don't convey the desired message, or even worse, can be misleading.

**Avoid**:

+ 3D charts
+ Race track, Donut, Pie chart: data is encoded on radius, but reader actually perceive area.
+ Zooming In: when using vertical bars, always start from 0. Otherwise it can make very small differences seem like big ones.

-----

## Project List

<details>
  <summary>1) Diamond Pricing</summary>
  The [dataset]() consists of 54,000 round-cut diamonds, with 10 Columns. For this exercise, we will focus on five variables: 1) price, 2) Carat, 3) Cut, 4) Color, and 5) Clarity - knows as the four 'C's of diamond grade. 
    The research questions guiding this analysis is the degree of importance that each of these quality measures has on the pricing of a diamond.
</details>

<details>
  <summary>2) Project: Ford Go Bike 2017-2019 </summary>
  This is the Final Capstone <a href='https://github.com/marcellovictorino/DAND_5_DataViz/tree/master/2_Project_%20FordGoBike'>Project</a> to complete the Data Analyst Nanodegree. It is an end-to-end data analysis project, going from the initial steps of data gathering and wrangling, progressing to a procedural Exploratory Data Analysis - investigating Uni, Bi and Multivariate relationship in order to extract meaningful insight - and finishing with polished visualizations to support telling a story.
  The final product is a Jupyter Notebook Slide Deck, allowing to easily share the project main findings with an html file.  
  
</details>

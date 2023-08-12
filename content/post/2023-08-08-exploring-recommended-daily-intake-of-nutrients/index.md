---
title: "Exploring The Recommended Daily Intake of Nutrients using FDA and NIH Data"
author: "John Lecocq"
date: '2023-08-08'
slug: "exploring-recommended-daily-intake-of-nutrients"
categories:
  - Health
tags:
  - NIH
  - FDA
  - Data Exploration
---

# Recommended Daily Intake 

Recommended daily intake (RDI) refers to recommendations as to how much of a given nutrient should be consumed by a person each day. RDI levels are set forth by authoritative sources, such as: the National Institutes of Health (NIH), the Food and Drug Administration, or other prominent medical establishments. This report explores RDI using data from NIH and FDA in order to understand which micro and macro nutrients have recommendations and what these recommendations are.

## Describing the Data

Two datasets were explored; one from the NIH website and one from the FDA. These datasets were available to the public at the time of writing this report. The data was fairly tidy to begin with, and not much processing had to be completed.

## Visualizing the Data

Visualizing data is the best way to gain a broad understanding of trends in data. For example, perhaps one will not be able to read, exactly, the microgram amount of Vitamin A recommended, but they will likely be able to identify that the milligram amount of Potassium needed is greater. See the figure below, and explore trends visible in the data. Keep in mind the colors represent different orders of magnitude masses (grams, milligrams and micrograms).

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_fda.png" alt="Bar chart of Nutrients and their recommended daily intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 1</strong>: Recommended daily intake of micro and macro nutrients according to the US FDA.</p>
</div>

The graph above shows the RDIs as recommended by the FDA. While it provides an easy to read and implement standard, it does not account for differences in demographics. The figure below, sourced via the NIH, does change their recommendations based on age and gender (RDIs for pregnant and lactating women are uniquely specified). Please, see the data below. It shows the same information as the plot above, but it is broken into four separate recommendations.

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_nih.png" alt="Bar chart of Nutrients and their recommended daily intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 2</strong>: Recommended daily intake of micro and macro nutrients according to the US NIH.<strong> Top Left </strong>Adults 4 and up, <strong>Top Right</strong> Children 1-3,<strong> Bottom Left </strong>Infants to 12 months, <strong>Bottom Right</strong> Pregnant and Lactating Women</p>
</div>

### A couple tips for exploring the data

- Notice that the x-axes of the figures above are logarithmic. Meaning, the bars between 100 and 1000 may be larger than they appear. 

- Also, notice that some nutrient RDIs were better reported using smaller units. Different units were color coded for easy viewing. 

# Exploring Trends

What lessons or rules of thumb can we learn from this data? The data itself is relevant to every human, but what jumps off the page may be different between people. Trends in the FDA and NIH data are discussed in the following two sections, respectively.

## FDA

Figure 1 above reveled the fact that the FDA RDI for protein and added sugars are the same. This begs the question: should one shoot for consuming the same amount of protein and the same amount of added sugars each day? Well, no, one must assume these RDIs are not strict guidelines, but are general rules of thumb. Each person, depending on their demographic data and goals, will develop individual nutrition guidelines to fit their needs. 

## NIH

We can see some of the personalization of RDIs evident in data provided by the NIH. Wherein, they individualize their recommendations based on 4 demographics. 

# Calculating Average Daily Intake

It is one thing to know what the RDIs for nutrients are, and it is another thing to know an individual's average daily intake (ADI) i.e. nutrients a person gets from their diet and supplements on an average day. To calculate ADI, one must determine:

1) The types of foods they eat and supplements they take on an average day,
2) How much of these foods they ingest 
3) The nutrition content of these foods and supplements. Once they calculate those values they may then calculate the difference in their ADI and the ROI for their demographic

Most people making these calculations would compare their ADI with the ROIs recommended by the FDA because the FDA data appears to be for adults (this was not confirmed, only viewed second-hand). However, parents will also want to refer to the NIH data to calculated the ADI-RDI differences for their children. A future report will go into detail into this process to aid the reader in calculating their ADI-RDI differences and determining if they need to cut back or supplement their dietary nutrient intake. 

Until then, take care, and God bless you in Jesus' name.
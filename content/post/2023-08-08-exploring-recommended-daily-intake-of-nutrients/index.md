---
title: "Exploring The Recommended Dietary Intake of Nutrients using FDA and NIH Data"
author: "John Lecocq"
date: '2023-08-08'
slug: "exploring-recommended-dietary-intake-of-nutrients"
categories:
  - Health
tags:
  - NIH
  - FDA
  - Data Exploration
---

# Recommended Dietary Intake 

Recommended dietary intake (RDI) levels are recommendations for how much of a given nutrient should be consumed by a person each day. RDI levels are set by authoritative sources, such as: the National Institutes of Health (NIH), the Food and Drug Administration, and other prominent medical establishments. This report used data from NIH and FDA to form a clear understanding of which micro and macro nutrients have RDI levels and what they are.

## Describing the Data

Two datasets were explored; one from the NIH website and one from the FDA. These datasets were available to the public, at the time of writing this report, in tabular form on the NIH's and FDA's websites. The data was organized well to begin with, and not much processing was be completed.

## Visualizing the Data

Visualizing data is the best way to gain a broad understanding of trends and differences in data. For example, perhaps one is not be able to read, exactly, the microgram amount of Vitamin A is recommended, but they will understand that the milligram amount of Potassium needed is greater. See the figure below to explore trends visible in the RDI data that was hard to see using only tables. Keep in mind the colors represent different orders of magnitude masses (grams, milligrams and micrograms).

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_fda.png" alt="Bar chart of Nutrients and their recommended dietary intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 1</strong>: Recommended dietary intake of micro and macro nutrients according to the US FDA.</p>
</div>

The graph above shows the RDIs recommended by the FDA. It is easy to read and can be useful for adults, but it does not account for differences in nutritional demands between different demographics of people. The figure below, from the NIH, accounts for age and gender (RDIs for pregnant and lactating women are uniquely specified). It shows the same basic information as the plot above, but it is broken into four separate recommendations.

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_nih.png" alt="Bar chart of Nutrients and their recommended dietary intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 2</strong>: Recommended dietary intake of micro and macro nutrients according to the US NIH.<strong> Top Left </strong>Adults 4 and up, <strong>Top Right</strong> Children 1-3,<strong> Bottom Left </strong>Infants to 12 months, <strong>Bottom Right</strong> Pregnant and Lactating Women.</p>
</div>

### A couple tips for exploring the data

- Notice that the x-axes of the figures above are logarithmic. Meaning, the bars between 100 and 1000 may be larger than they appear. 

- Also, notice that some nutrient RDIs were better reported using smaller units. Different units were color coded for easy viewing. 

# Exploring Trends

What lessons or rules of thumb can we learn from this data? There is information relevant to every human, but what jumps off the page is likely to be different between people. Some trends in the FDA and NIH data are discussed in the following two sections, as examples of how this data may be interpreted.

## FDA

Figure 1 showed that the FDA's RDI for protein and added sugars are equal. This begs the question: should one shoot for consuming the same amount of protein and the same amount of added sugars each day? Well, probably not, one must assume these RDIs are not strict guidelines, but are general rules of thumb. Each person, depending on their demographic and physiological goals, will develop individual nutrition guidelines to fit their needs. 

## NIH

From 30,000ft., the NIH data shows that infants require all the same nutrients as other groups, but, generally, in smaller amounts. **For example, the comparison graph below (figure 3) shows that infants require smaller amounts of most nutrients, excepting vitamin A, vitamin C, iron and iodine.** Infants require more of these nutrients than small children do. 

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_nih_2.png" alt="Bar chart of Nutrients and their recommended dietary intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 3</strong>: Comparison of recommended dietary intake of nutrients between groups. Data from the NIH. The left side shows amounts in milligrams (MG) and the right side shows amounts in micrograms (UG).</p>
</div>

# Calculating Average Dietary Intake

It is one thing to know what the RDIs for nutrients are, and it is another thing to know an individual's average dietary intake (ADI) i.e. nutrients a person gets from their diet and supplements on an average day. To calculate ADI, one must determine:

1) The types of foods they eat and supplements they take
2) How much of these foods they ingest 
3) The nutrition content of these foods and supplements. 

Once they calculate those values they may then calculate the difference in their ADI and the ROI for their demographic. This information can be used for guiding dietary decisions for better health. Most people making these calculations would compare their ADI with the ROIs recommended by the FDA because the FDA data appears to be for adults (this was not confirmed, only viewed second-hand). However, parents will also want to refer to the NIH data to calculated the ADI-RDI differences for their children. 

A future report will go into detail into this process to aid the reader in calculating their ADI-RDI differences and determining if they need to cut back or supplement their dietary nutrient intake. Until then, take care, and God bless you in Jesus' name.

---
title: "Recommended daily intake of micronutrients"
author: "John Lecocq"
date: '2023-08-08'
slug: "exploring-recommended-dietary-intake-of-nutrients"
categories:
  - Data Exploration
tags:
  - Nutrition
---

# Recommended Dietary Intake 

Recommended dietary intake (RDI) levels are recommendations for how much of the essential nutrients should be consumed by a person each day to meet their nutritional needs. Essential nutrients are those that have been shown to be necessary for homeostatic continuity i.e., needed to avoid nutrient deficiency sicknesses, based on known biochemical pathways or, at least, significant experimental data [](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4717892/#:~:text=The%20first%20RDAs%20for%20protein,Defense%20Advisory%20Commission%20(11)) **This report is intended to help the reader form a clear understanding of which micro and macro nutrients have RDI levels and what they are.** It is a predecessor report to one that will show how to calculate dietary nutrient intake.

## Materials and Methods

Data from the NIH website was explored [(1)](https://www.fda.gov/media/99069/download). The data was available to the public, at the time of writing this report, as tables on their respective websites. The tables were copied into Microsoft Excel, and data visualization was completed using R. 

## Data Visualization

The figure below shows the RDI levels for different demographics, data from the NIH [(1)](https://www.fda.gov/media/99069/download).

<div class="figure">
<img src="{{< blogdown/postref >}}index_files/plots/RDI_plot_nih.png" alt="Bar chart of Nutrients and their recommended dietary intake." />
<p class="caption"><span id="fig:weight_time"></span><strong>Figure 1</strong>: Recommended dietary intake of micro and macro nutrients for 4 demographics.<strong> Top Left </strong>Adults 4 and up, <strong>Top Right</strong> Children 1-3,<strong> Bottom Left </strong>Infants to 12 months, <strong>Bottom Right</strong> Pregnant and Lactating Women.</p>
</div>

## Tips

- The x-axes of the figure above is logarithmic. Meaning, the bars between 100 and 1000 are larger than they appear. 

- Some nutrient RDIs were reported using smaller units. Different units were color coded.

# Exploring Trends

From 30,000ft., the NIH data shows that infants require the same nutrients as other groups, but in smaller amounts. **However, viewing the data above in a different way (figure 3), one can see that infants require the least amount of most nutrients, excluding for vitamin A, vitamin C, iron and iodine.** Those, they require more than young children (1-3).

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

**It is one thing to know what the RDIs for nutrients are, and it is another thing to know an individual's average dietary intake (ADI)** i.e. the average amount of nutrients a person takes in through diet and supplements each day. To calculate ADI, one must determine:

1) The types of foods they eat and supplements they take
2) How much of these foods they ingest 
3) The nutrition content of these foods and supplements

**Once a person calculates the values above, they can calculate the difference in their ADI and the ROI for their demographic.** This calculation can guide their dietary decisions to improve overall health and well being. A future report will go into detail into this calculation to aid the reader in calculating their ADI-RDI differences and determining if they need to cut back or supplement their diet. Until then, take care, and God bless you in Jesus' name.

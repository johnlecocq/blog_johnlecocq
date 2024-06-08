---
title: Interative application for dietary analysis - macro and micronutrients
author: 'John Lecocq'
date: '2024-06-05'
slug: interative-application-for-dietary-analysis-macro-and-micronutrients
categories: ['Web Apps']
tags: ['Dietary Analysis', 'RShiny']
---

# Dietary analysis

The science of dietary analysis is not new, but it has been expansively built upon in modern times due to advanced analytical chemistry techniques and computers. It is at such a point now that almost every food imaginable has been analyzed for its nutritional content and this data is available from the US Department of Agriculture. Combining that data with reference intakes, available from many sources, one may gain context into how their diet stacks up nutritionally.

# Nutrient calculations

Calculating the amount of nutrients contained in a set of foods is a simple application of mathematics. For example, consider a calculation of the nutrient content of a cup of frozen blueberries. One must look through the foods data to find blueberries and find the nutrient content contained in them. The only additional step needed is to adjust the serving size of the blueberries to the amount one actually consumed. This process of looking up foods, their nutrient contents and scaling by serving sizes is enough to complete a full day's dietary analysis. If your memory and math are sharp, then consider giving the application below a try to learn more about the nutritional content of your favorite foods.

# App for dietary analysis 

The application below aids it user in a dietary analysis. Interacting with its simple interface, the user can accurately and quickly estimate the nutrient content of their diet and reference those values against established daily reference intakes. Using the application well will require some thought and a few calculations, but the little bit of work, up front, pays off in a deeper understanding of the foods one eats every day.

# Instructions and app

To begin using the app, select from the first dropdown your lifestage group or the lifestage group of another person who could be your child, spouse or parents. Next, you will enter the number of food items you plan to enter. For example, a fruit smoothie I made this morning contained 6 ingredients: water, blueberries, strawberries, bananas, almond butter and when protein, so I would enter 6 to analyze the nutrient content of the smoothie. 

Next is the part that will likely take some getting used to, but is simple once you understand what's going on. This part is food selection. The available number of foods is large so a search bar will help you narrow down the data. For example, if I were to look up water in the dropdown, I would search - water, - the comma being important. Also, if I were to search for frozen blueberries, I would search - blueberries, - the s and the comma being important. Unfortunately, the search feature does not behave like Google so there is a bit of a learning curve. After a short while, though, one will find the rhythm of the data and looking for foods will become easier. Remember, that if you cannot find what you are looking for then maybe be less descriptive and look for the right choice. For example, let's say one is looking for lean ground beef they can narrow down their choices by typing beef in the search bar, understand how the data is categorized generally and then try to match the pattern. While the search is not case sensitive, it is sensitive to the order of characters which is why the comma will often matter. You will see what I mean!

It gets easier from here, but there are quirks that need to be mentioned. The main quirk of the diet adjustment page is that if you add/remove/change a food, then the serving size selections will reset. Meaning, if you put water and selected a serving size of 8 fl oz, then if you add/remove/change a food selection dropdown, the serving size selection will be reset to the default. There are several checks for this, the last line being the section at the bottom of the diet adjustment page which lets you tell the computer how much of a serving of a food you had e.g. did you have 1 cup of water or 10. At that area, one will find the food that was selected and the portion size. Check that the foods and portion sizes are sufficient, then enter a number which scales the portion size. This is where some math and estimation will come into play. One may enter decimal values (no fractions sorry) into these boxes if they had, say, a half cup of blueberries; enter 0.5 or any decimal that you find is correct.

# Have a ball!

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/3.5.16/iframeResizer.min.js">
</script>
<style>
  iframe {
    min-width: 100%;
  }
</style>
<iframe id="myIframe" src="https://invo.shinyapps.io/nutrientCalculator/" scrolling="no" frameborder="no">
</iframe>
<script>
  iFrameResize({
    heightCalculationMethod: 'taggedElement'
  });
</script>
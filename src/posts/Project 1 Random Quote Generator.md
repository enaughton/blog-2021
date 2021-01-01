---
title: Project 1 Random Quote Generator
summary: Random Quote Generator
date: 2020-03-28
tags:
  - projects
  - javaScript
  - tech degree
  - developer
---

# Goal: To Display a "Random" Quote on the Screen

### [Click me to see a Live Link](https://enaughton.github.io/Random-Quote)

### [Click me to go to the RepoGithub Link](https://github.com/enaughton/Random-quote)

- Step 1: Create the array of quotes you want to display

  In the Array, You will break them up into Quote, the movie, and the year the movie came out.

  ![An Array of Quotes](/images/project1/array.png)

- Step 2: Select the "Random Quote"

  We create a function called getRandomQuote.

  3 variables used in this function (number, randomQuote, and source)

  Math.Floor() returns the largest whole number less than or equal to a given number

  Math.Random() returns a random decimal number between 0 and 1

  We take the number in our quotes array, which selects a quote in the array

  Then we return the variable randomQuote

![getRandomQuote function](/images/project1/getRandomQuote.png)

- Step 3: Print The Quote to the Screen

  Create another function called printQuote()

  We store the quote, the movie, and the year into their own variables.
  Now we need to use a variable called print. print creates a template that will be used to display the quote/source/year/citations.

  Next, we add a couple if statements. if there is a citation we add that to the print variable, and if there is a year in the quote add it to the print variable.

  The wrap up this function we select an HTML Element by ID and use innerHTML to inject the print's HTML template into the HTML file.

![printQuote function](/images/project1/printQuote.png)

- Step 4: Finally Call the printQuote Function

  This is the final bit! Call `printQuote()`

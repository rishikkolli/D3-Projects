# International Football Results Extra Credit Assignment 

In light of the recent world cup, in this assignment you will apply your knowledge of D3 animations and joins to create a unique bubble chart visualization that explores the home team, away team, and goal differential for all international matches between `1916-2022`. This assignment is worth 10 points and will consist of:
- Donwloading the [International Football Dataset](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017) from Kaggle
- Displaying a bubble chart visualization based on HTML controls where the user can select a specific home team to explore their results throughout the years against different international opponents
- The user should be able to hover over a specific bubble and see the goal differential displayed with a positve number depicting a win and a negative number depicting a loss and the team that they played using a tooltip
- The visualization should have a unqiue custom color key displayed to the side of the visualization (especially distinguishing wins from losses and any other distinictions of your choosing) explaining the colors of the bubble
- Each bubble should have a unqiue color respresenting the result of the goal differential matching the key you have built
- Additionally there will be a transition displaying each match result (bubble) in ascending order over years once the user clicks the submit button alongside animated transitions of the axis 
- Finally, since there might be multiple international matches we would like to implement a [brushing for zooming](https://d3-graph-gallery.com/graph/interactivity_brush.html#brushingforzoom) feature on our bubble chart

I would suggest you take advantage the [D3.js Graph Gallery](https://d3-graph-gallery.com/index.html) as a Starting Point for implementing this project in D3 V7 and exploring how do your tasks, now lets break down this project

Alright lets get cooking!

## Step 1: Analyze and break down your dataset (import and wrangle)
- Download the [International Football Dataset](https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017) from Kaggle
- Create a data folder and drop your csv within your data folder
- Next, look into how bubble charts are built (HINT: they deal with three changing variables and their relationships)
- In our case we will look into date, away teams played against, and goal differential
- Goal differnetial explores the difference between goal(s) conceded and goal(s) scored (TWO HINTS: each row represents a goal [look into the team column] -> might need to do some calculations, there are never two international matches that the home team you choose will play on the same day)
- Certain years are not even mentioned in this dataset keep that in mind when setting your range of years

## Step 2: Build the Initial Landing Page
- Similar to previous assignments, make sure to include your name, email, and assignment number at the top
- You can choose the size of your SVG or the div holding your SVG but make sure to keep it appropriate, we will be building a zoom in feature so don't stress ;)
- Create a `select` dropdown for choosing the home team to analyze. Provide a default value of United States, AKA the greatest football team to set foot on this planet
- Build a play button to append circles onto SVG. One way to do this is with an `<input type='button'>` element. They play button will be clicked to append each circle.

## Step 3: Setting your Axis and layout for the bubble chart
- Your x-axis will be timestamps for years and deal with years for matches based on the range of years each team played
- Your y-axis will consist of a list of all opponent teams that the home team you selected competed against
- +1 point extra credit for arranging the opponent teams in alphabetical order from top to bottom on the y-axis
- What do bubble size and color represent?
    - The bubble size represents the size of the goal differential in this drawing
    - The color of the bubble represents whether the user won or lost their respecive games or if the goal differntial was positive or negative

## Step 4: Bubble Chart Interactions
- We are looking for three animations or interactions in this drawing
- One animation is customized [axis transition](https://bl.ocks.org/HarryStevens/678935d06d4601c25cb141bacd4068ce) for the max or min year for each specific home country in the games they might have participated in, in this case we are looking at the y-axis or date
  - Specifically I would like you to re-draw and remove or add years by shifting the time stamps in year
  - This animation should be paused and should take around 500 ms
- Another animation is a customized [axis transition](https://bl.ocks.org/HarryStevens/678935d06d4601c25cb141bacd4068ce) for the x-axis where the away countries need to be reshuffled and remove non-exsistent opposing teams by fading them out
  - This animation should be paused and should take around 500 ms
- The third animation will be to draw and append the circles in an ordered manner from left to right with games/bubbles placed in chronological order from 1872 to 2022
- All these animations should be activated once the user selects to click the submit or play button

## Step 5: Creating the Key for Pie Chart
- Create a bubble chart legend which explains the color and size of the input similar to this [link](https://d3-graph-gallery.com/graph/bubble_legend.html)

## Step 6: Zoom In Feature
- Create a zooming application that allows the user to hover over a specific section and the y-axis expands to see each bubble in that specific visualization
- Use this website for guidance [link](https://d3-graph-gallery.com/graph/interactivity_brush.html#brushingforzoom)

+2 Extra Credit for innovative design and landing page

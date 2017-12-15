# Lab 02: Adding User Interaction to a Leaflet Choropleth Map

## Part I. Building an interactive map (8 points)

**Instructions:** Begin with the starter template *index.html* file located within the */lab-02/* directory. Beyond the starter template *index.html* file, this directory includes the *data/ky_counties_housing.json* data file and a metadata file *data/ky_counties_housing.txt* (also used in Module 01).

Modify the *index.html* to fulfill the requirements listed below.

This lab follows the instructions detailed within Lesson 02 to extend the map created in Lab 01 to include greater user interaction.

Specifically, the map will allow the user to select a new data attribute, which will trigger the map and update the legend using this data attribute. The map will also provide the user with an info panel that, upon mousing over the counties, will provide the user with the raw data (i.e., non-normalized data values) associated with each county. To achieve this, carefully follow the instructions detailed in Lesson 02. The HTML, CSS, and JavaScript written within your completed *index.html* file should additionally achieve the following:

1. Build a map allowing the user to explore data related to **vacant** housing units, as opposed to the occupied ones used in the Lesson 01 and Lesson 02 examples (refer to the metadata file *ky_counties_housing.txt* for a description of data property names).

2. Provide a visual affordance for when the user mouses over individual counties, beyond the appearance of the info panel and the tooltip popup. Changing the color of the county's stroke (i.e., from gray to yellow), is recommended, as this allows the user to still see the color symbolizing a normalized data value, though you may explore other options for such an affordance (such as county color fill).

3. Finally, *thoroughly comment your JavaScript code*. The purpose of these comments is to demonstrate that you understand the code you've written. Think of this as writing comments for one of your classmates that will explain what the code is doing. **Note**: this is a key part of this task and will be graded accordingly. Use the comments written within the starter template for lab 02 as guidance.

4. Ensure that all your code is well-maintained with indentions and appropriate whitespace to improve human legibility. Hint: install and use the [Atom atom-beautify package](https://atom.io/packages/atom-beautify) or [Brackets Beautify extension](https://github.com/brackets-beautify/brackets-beautify) through the Extension Manager to help clean up the indentions and spaces within your HTML, CSS, and JS.

Save your changes to your *index.html* file and **commit changes to your local GitHub repository** as you work.

## Part II. Understanding the lesson (2 point quiz)

Create a new file named *quiz-02.md* within your *lab-02/* directory, and provide short answers (1 - 2 sentences) to the following questions within it. This is a markdown file, and you'll be writing plain text or markdown within it.

### Quiz

1. Within the starter *index.html* file, we declare and define the variable `dataLayer` before calling the `getClassBreaks()` function. Why do we do this?
2. How does the JavaScript detect a change in the HTML select option? Be specific.
3. The `drawLegend(breaks)` function in the starter *index.html* file contained a parameter, `breaks` in its definition. But when when refactored the script for lesson 02, we can remove this parameter. Why?
4. In the completed lesson 02 script, we use Leaflet's `.eachLayer()` method within both the `drawMap()` function and the `updateMap()` function. Why do we have the code that updates our info panel information within the `drawMap()` function rather than using the `.eachLayer()` method within the `updateMap()` function?

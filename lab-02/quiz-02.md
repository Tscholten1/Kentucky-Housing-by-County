1.	Within the starter *index.html* file, we declare and define the variable `dataLayer` before calling the `getClassBreaks()` function. Why do we do this?

By creating the dataLayer before we call the `getClassBreaks()` function, the code provides the essential information/data from which the getClassBreaks is able to retrieve or reference data on which to create the class breaks. Essentially, the function loops through the dataLayer to determine a reference data for getClassBreaks. 

Yes, `dataLayer` references the GeoJSON data properties, which we then use to calculate the class breaks for a given attribute.

2.	How does the JavaScript detect a change in the HTML select option? Be specific.

The JQuery `.on()` method is an event listener which “detects” when a user changes some element of the map such as clicking on radio buttons, drop down menu items, or sliders. In Lab 2, we detect when the user has changed the dropdown selection. We then use the JQuery method `.val()` to pull the currently selected data attribute from the selected option and reassign the value of the global variable `attributeValue`. We can then redraw the map using this variable.

3.	The drawLegend(breaks) function in the starter *index.html* file contained a parameter, `breaks` in its definition. But when when refactored the script for lesson 02, we can remove this parameter. Why? 

The geometries (e.g. state of Kentucky counties and boundaries) need only be drawn once, but when the user selects different data attributes, the data must be reclassified and updated repeatedly.

Yes. Well put.

4.	In the completed lesson 02 script, we use Leaflet's `.eachLayer()` method within both the `drawMap()` function and the `updateMap()` function. Why do we have the code that updates our info panel information within the `drawMap()` function rather than using the `.eachLayer()` method within the `updateMap()` function?

The information that is displayed in the info panel is derived from ghosting over Kentucky counties rather than changing the variable in the data variable drop down menu. The code in that updates the information is assisted by using the drawInfo function.

The information in the info panel isn't updated when the user changes a dropdown selection. Therefore it doesn't need to be updated when the map and legend are.

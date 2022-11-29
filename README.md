# UFOs

## Project Overview
This project will create a filterable table that will display UFO sightings from across the world. There are options to filter this data by:

- Country 
- State 
- City 
- Shape 

The data for the table will be kept in a javascript file, and will be displayed on an HTML webpage using Javascript filters and Bootstrap/css customizations to add visual elements and images. The page will also a banner, title and short paragraph explaining the project.


## Source Materials
- Data Source: /static/js/data.js
- Javascript file: /static/js/app.js
- Images: /static/images/nasa.jpeg
- CSS: /static/css/style.css
- HTML: index.html
- Software: Python 3.6.1, Visual Studio Code, 1.38.1

## Results
Using out Javascript file app.js, we were able to create several functions which looped through our data to build a table and filter our data. First, we used a d3 selector to select "tbody" from our index as the table referece. Next the function buildTable() clears out existing data loops through each object in our dataset to create the inital table. This is what our users initially see when they go to the webpage:
  ![UFO Init](https://github.com/ecost95/UFOs/blob/main/Screenshot%20(227).png)

Next, the function updateFilters() uses d3 select to save the element that was changed as a variable, and save the id of the filter that was changed as a variable. If a filter value was entered then the function adds that filterId and value to the filters list. Finally, it applies all the filters to rebuild the table. 
The filterTables() function loops through all of the filters and keep any data that matches the values in our data. It applies a d3 event to listen for changes to each filter, then rebuilds the table. 

Here is an image of our table when filtered by state: ca and city: el cajon:
  ![UFO Filtered](https://github.com/ecost95/UFOs/blob/main/Screenshot%20(224).png)


## Summary
The project results are satisfactory and the webpage functions as expected. However, there is still room for improvement for this project. 

For one, we could improve the filter table by adding a button that says "Filter". This would allow users to type in their search criteria, check for spelling errors, and only show them results when they click the button to filter. To do this, we could add a Bootstrab button element to the index.HTML and create an event listened for the button "on click".

We could also add additional an additional style references to our index.html to add more customizations, including new fonts for different elements (table, paragraph, title, etc).

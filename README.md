# scoreApp


1. Create a local array of data objects with the following properties:
    id: number; // unique identifier
    name: string; // name of a person like 'Bob';
    score: number; // numerical score between 1-100;
    date: string; // string representation of a date. For example, Oct 21, 2016 will be "2016-10-21"; 

    When creating your data, id should be unique, names should be randomly picked from a list of 4 ( which  you can chose ), 
    scores should be generated randomonly from between 1-100, dates should  be generated randomly from between Jan 1st, 2016 and Dec 31st, 2016

    Use this as your data source for your application instead of an actual backend api.

2. Create an Angular app, ( 1.x or 2/4 ) with the following features:

   -Displays one page.

   -Has a list of filters: name, begging date, ending date. The filters are dropdowns that should be populated with options from 
   the available data generated in step 1.

   -Under the filters is a d3 ( https://d3js.org/ ) historical bar chart.  The y axis is 'score'.  The x axis is 'date'.  ( you can use http://krispo.github.io/angular-nvd3/#/ instead of working directly with the d3 api's as long as you are using angular 1.x )

   -If no name is selected in the name filter than a message says, "Please select a name" where the bar chart would appear.

   -If a name is selected but no begining or end dates are selected then the bar chart shows all the scores for the selected name.

   -If a beginning filter is selected then all the scores for the selected name are show from the beginning date.

   -If an ending filter is selected then all the scores for the selected name are show up to the end date. 

   -If both beginning and end filters are selected than the range of scores are shown. 

3.  After getting #2 to work you will add voice recognition using the free voice recognition api in chrome. 

    -Add a voice toggle button.  
    -When voice is toggled on, the filters are disabled and a search box appears.
    -When voice is toggled off, the filters are enabled again and the search box disappears.
    -When voice is toggle on, the search box populates with what the user says and should be ble to handle these simple phrases: 

    'Show me all scores for [name]'
    'Show me all scores for [name] from [beginning date]' ( month and year are enough )
    'Show me all scores for [name] up to [ending date]' ( month and year are enough )
    'Show me all scores for [name] between [beginning date ] and  [ending date]' ( month and year are enough )

    If the app does not recognize the phrase then some feedback is given to the user asking for a clearer message.

    Here is a simple tutorial to explain how to get voice recognition working in chrome: https://developers.google.com/web/updates/2013/01/Voice-Driven-Web-Apps-Introduction-to-the-Web-Speech-API



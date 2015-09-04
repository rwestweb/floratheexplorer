# Flora The Explorer

Introduction
------------

The Colorado Plants project is a web application designed to gather data about wild plants growing in Colorado. The application will be available to the general public for data entry. No registration or login will be required to access this page. Additionally, a data reporting page will be available but access to this page will be password protected.

The application will be accessible using a web browser only, but must be usable on a tablet, phone and PC.
 
Problem Statement
----------

We’re solving two problems:

1. An inefficient way of collecting data from users.
2. An inefficient way of browsing the collected data.

Currently, users must fill out an outdated excel sheet that incites exhaustion at its very sight. Additionally, there is now way to browse the collected data other than going through each excel sheet one by one.

Our app will streamline both functions by exploiting web technologies to make data collection easier for users and provide reporting functions for administrators.

Data items
----------

The following data items will be collected.

- User name - text field, restricted to alphabetical characters, 30 characters max
- Plant name - text field, restricted to alphabetical characters, 30 characters max
- Plant location - text field, restricted to alphabetical characters, 50 characters max
- Observation date - text field, restricted to date format 'mm/dd/yyyy'
- Observation time - text field, to collect hours, restricted to numbers, 2 digits max
  - text field, to collect minutes, restricted to numbers,  2 digits max
  - drop-down list with options AM and PM
- GPS Coordinated - hidden or non-editable field, populated by WEB API
- current Time stamp - non-editable field, populated with current server date and time
- Weather conditions - text field, restricted to alhabetical characters, 30 characters max
- Current Temperature	- text field, restricted to number only, maximum 3 characters, labeled Fahrenheit.
  - **Note**: *If Observation date and time are within one hour of the current time, weather conditions and temperature could be collected using an API provided by weather.com or a similar site.*
- Soil Type - drop-down list with options (see spreadsheet)

**Notes** - *a free form text field to allow user to enter additional information he/she may want to add. This data cannot be validated, but there is a desire to exclude profanity. HTML or other mark up tags will also be excluded, for security reasons. 128 characters max.*

Data collection and form processing
-----------------------------------

User name, plant name and soil type will be required information. All other fields are optional.

Initially weather data and location data will be entered by the user. If time permits, this data will be collected using a web application.

The data will be saved when the user clicks the Save button. Once the current record has been saved, the form will be re-displayed preserving all fields except plant name, notes, and soil conditions.

If time permits, we may populated weather conditions using a web app. even if observation time and system time are more than 1 hour apart. If this can be done, the user entered weather condition and temperature fields will be eliminated. 

Reporting Page
--------------

The data reporting page will be password protected. Once the correct password has been entered, all records currently in the database will be displayed, sorted by the stored system time stamp, newest record first. A button will allow the user to download the data. Download format will be limited to a comma delimited file (CSV) initially. If time permits, other formats such as PDF may be added.

Technical Resources
----------

### Back End Dependencies

- Linux Apache2 MySQL PHP (LAMP Stack)

### Front End Dependencies

- HTML, CSS, JavaScript
- [jQuery](https://code.jquery.com/)
- [Twitter Bootstrap](http://getbootstrap.com)
- [Modernizr](http://modernizr.com/)

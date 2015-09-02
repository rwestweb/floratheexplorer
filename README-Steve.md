# Flora The Explora
## Requirments
### Back End Setup
- LAMP Stack
### Front End Dependencies
- [jQuery](https://code.jquery.com/)
- [Twitter Bootstrap](http://getbootstrap.com)
- [Modernizr](http://modernizr.com/) 
## Problem Statement
We’re solving two problems:
- An inefficient way of collecting data from users.
- An inefficient way of browsing the collected data.

Currently, users must fill out an outdated excel sheet that incites exhaustion at its very sight. Additionally, there is now way to browse the collected data other than going through each excel sheet one by one.

Our app will streamline both functions by exploiting web technologies to make data collection easier for users and automating several of the manual tasks admin currently has to take to browse the collected data.
## Data collection
### Front End (HTML, CSS, JS)
The Front End has two main tasks.

First, it must collect following the data:
- Name of user
- Date gathered
- Name of plant
- Soil conditions
- Current weather
- Location
- Additional notes

There are two ways users can upload this data:

- While they are in the field as they make observations in real time.
- Post hoc.

While in the field, we can make use of browser technology and free weather APIs to accurately report the user’s location and weather conditions, thereby minimizing the effort required to upload the data. A real-time record upload will require the front end to be mobile responsive.

A post hoc record upload will require the user to enter location and weather data.

The second Front End task is to display the uploaded records (*no querying necessary*). This data will protected by a single code.
###Back End (PHP)
The back end will add the following to the uploaded record:
- UID
- Time Stamp

After adding that data, the back end will connect to and upload the data to a MySQL database.

In addition to injecting data to the database, the back end will authenticate admin personnel as they seek to browse the data.

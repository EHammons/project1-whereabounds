# whereabounds app
> Web app for displaying user-submitted city details including weather, maps, places and more.
## Deployed App
https://ehammons.github.io/whereabounds/

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Group Members](#group-members)
* [Contact](#contact)

## General info
Created for a coding class project, all group members have collaborated to create a working, useful all-in-one app to give a user information about their selected city.
<br><br>
Follow this link to view our group [presentation](https://docs.google.com/presentation/d/135A7quBTscWsDuqAyqq_Ttr0lWsFq7YlAnIDnlk06Rs/edit?usp=sharing).

## Screenshots
![Screenshot](./assets/images/Project_One.jpg)
![Screenshot](./assets/images/deployed.png)

## Technologies
* Weatherbit API - v2.0
* Google Places API
* Google Maps API
* jQuery
* JavaScript
* HTML5
* CSS3
* Bootstrap

## Code Examples
    if (results[i].rating !== undefined) {
        var placeRatings = results[i].rating;
        var starTotal = 5;
        var starPercentage = (placeRatings/starTotal) * 100;
        var starPercentageRounded = (Math.round(starPercentage));
        var stars = $("<div>");
        stars.addClass("stars-outer");
        var place = $("<div>");
        place.addClass("stars-inner");
        $(stars).append(place);
        $(place).width(starPercentageRounded+"%");
        ratingDiv.append(stars);
    }

    function geocodeLatLng(address) {
    geocoder.geocode({'address': address}, function(results, status) {
    if (status === 'OK') {
        if (results[0]) {
            var lat = results[0].geometry.location.lat();
            var lng = results[0].geometry.location.lng();
            displayCity(lat, lng);
            var latlng = lat + "," + lng
            // here is where we can call other functions, it's the 'good' path
            findPlaces(latlng);
            return latlng;
        } else {
            console.log('No results found');
        }
        } else {
            console.log('Geocoder failed due to: ' + status);
        }
        });
    }


## Features
List of features ready and TODOs for future development
* User input city results in:
* Five day weather forecast
* Five places to visit

## Status
Project is: _finished_

## Inspiration
Inspired by a vision of culture at your fingertips.
Based on the project 1 assignment for The Coding Bootcamp at UT Austin.

## Group members:
* Elise Hammons: https://github.com/EHammons
* Kristen Stroup: https://github.com/Knwhit20
* Aaron Phillips: https://github.com/aaronphillips929
* Christopher Mlinac: https://github.com/cmlinac

## Contact
Created by Elise Hammons (and project group 1) - feel free to contact me!
<br>[LinkedIn](https://www.linkedin.com/in/elise-h-01243258/)
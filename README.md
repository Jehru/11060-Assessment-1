# 11060 – Assessment 1 API Sketch (Jehru Harris / U3202988)

### Github Pages Url:
https://jehru.github.io/11060-Assessment-1/
\
\
\
## Reflection on development process

The full development process can be found in the Appendix A.  

I initially began this project with research, one topic I discovered was visualising cultural collections and displaying cultural data. In a ted talk by Mitchell Whitelaw (Whitelaw, 2010), he described how we should display and conserve our digital cultural data. Some of the key concepts that I learnt from this research was how as a designer   you can change how people explore information on a web interface. And how our traditional models of searching for information don’t always work that way in the real world, for example in a museum you don’t go in looking for one specific item but rather want to explore what exists in a particular theme or topic. My takeaway is how as designers we should think how we display data in websites similar to the real world. (Whitelaw, 2010)
\
\
\
In my development process I found that choosing a theme helped to give the website structure and gave the website a consistent look and feel. 
I found that after working with several API’s the Geolocation API took some working out as the Google Cloud system requires you to toggle a button on/off to enable that feature from the URL. 
The Amphibaiweb’s audio files used an underscore between the species name in their audio URL’s so when I found the ‘link identifier’ data (which returned the species name with an underscore in between) in the Atlas of Living Australia (ALA) API this was very helpful as it reduced the coding required on switching a space to an underscore. This link identifier complimented the Amphibiaweb sound URL’s. 
Despite having to use a CSS framework that I am not familiar with I found the UI Kit framework to be easy to learn as their framework is well documented. I also found that it worked better than using a framework such as Bootstrap which would require me to add a row for each 3 or 4 items. UI Kit was easy to implement as all the frog cards had the same div classes. 
\
\
\
One of the major issues that I struggled with in this project was finding a good API. I felt that the API had to include images to make it visually engaging for the viewer. After finding the ALA API I discovered that it is not well documented despite this I found extra documentation which allowed me to create the functionality that was needed for the website. 
One other issue that I encountered was that every item that was appended to the page all used the same div tag and class name, this created issues with when the user clicked on one of items. It would trigger all the items in the page at once. This issue also persisted when images were not found the website would not return any images at all. I initially used the image=’onerror(function)’ which didn’t work but I found the jQuery method of .on(error) to work. I solved the on click problem by the .find() and toggle() method to toggle a hidden text class on the class item.
\
\
\
One of the main takeaways from this project was the importance of locating the right API for the project and that a well-documented API makes the development easier. I also learnt how to use jQuery to add and remove html items from a page. 

Prior to this project I had no previous knowledge of GLAM data and through this project I am now interested in taking GLAM data which traditionally (especially younger audiences) viewers may find uninteresting or disengaging and redesigning it to be explored with in a new and interesting way. 
\
\
\
## Design decisions 

The colour palette consists of a monochromatic green and a complimentary pink. 

![Colour Palette](/assets/rationaleImages/colourPalette.png)
_(Coolors - Colour Palette, n.d.)_

All colours were tweaked colorsharks contrast tool. This tool gives advice to making your text and background colours WCAG 2.1 compatible. (Riggan, n.d.)

These colours were chosen with green as the primary colour as frogs are frog stereotypes are green, however at the end of the project I noticed that frogs near Canberra are usually more brown/grey in colour. The complimentary pink was chosen to contrast and stand out against the green. 

The UIKit cards were left as the default as I preferred the white and grey colours over my previous design which used a light green and dark green. I felt that the white looked more professional and contrasted better against the mint green background. 

The main function of the webpage is to display frogs that have been reported geographically near the user. The site has no additional pages to maintain simplicity and utilises a balanced symmetrical layout. The interface was designed to be user friendly easy for the user to navigate. 

The typeface chosen is Poppins, which was chosen due to its round friendly look. Poppins is an easy-to-read sans serif geometric typeface that gives the site a modern look. I wanted a friendly looking typeface to compliment the frogs that I was showcasing.  

I used a card style interface to show the frog images and information. This was implemented as it would provide a similar experience when using the site on the desktop or mobile. I was originally going to hide all the information behind the image and only show when the user clicks on it but felt that it was necessary to provide some information. 
\
\
\
## Examples of other relevant interfaces

The best 3 examples are shown here, more examples can be seen in the Appendix B.
I was inspired by the Apples at the Met, Ceramic Beats and Buddhas at the Met sites. All these websites are student projects and inspired me to build an interactive and engaging website.  

![Apples of the Met](/assets/rationaleImages/applesOfMet.png)
_(Apples of the Met, n.d.)_

![Buddhas of the Met](/assets/rationaleImages/buddhasAtMet.png)
_(Ceramic Beats, n.d.)_

![Ceramic Beats](/assets/rationaleImages/ceramicBeats.png)
_(Ran, n.d.)_

## References

Apples of the Met. [Image]. Retrieved from https://xingwei726.github.io/Major-Studio-1/Week10_InteractiveProject/test8/#page-1

Ceramic Beats. [Image]. Retrieved from https://azuic.github.io/CeramicBeats/

Coolors - Colour Palette. [Image]. Retrieved from https://coolors.co/d8f3dc-298561-074a35-081c15-df5979

Ran, D. Buddhas at the Met [Image]. Retrieved from https://shuvitran.github.io/MajorStudio1/Project2-qualitative/FrontEnd/

Riggan, M. ColorShark – WCAG 2.1 AA and AAA Color Contrast Tool. Retrieved 19 March 2021, from https://colorshark.io/

Whitelaw, M. (2010). TEDxCanberrra - Mitchell Whitelaw - Visualising culture [Video]. Retrieved from https://www.youtube.com/watch?v=i8JO0KkYvow
\
\
\
## Appendix A
#### Full Process

I started this project by researching the basics of jQuery and how to use API URL’s. I watched the jQuery Essential Training video (Marini, 2016) and another course, Intro to jQuery on Udacity (Intro into jQuery, n.d.). I completed the GitHub profile API tutorial (Rocheleau, 2013) and found it very helpful in understanding how to query and retrieve information from an API.  

I created my website by following a tutorial that used the OpenWeather API however as our class content changed to GLAM API’s I researched the Trove API, and I was able to transfer my previous code to the Trove API by changing a few lines of code. (Vieira, 2020)

By using various array and object methods to target the values I realised how to print out the results to the console, then to the page. For example ‘console.log(data.results);’ would print the amount of items that was found in that API call.

At this stage I realised that the Trove API had no images, I then decided to find a different API. I decided that images were necessary to make the site visually engaging. There are other ways to represent data visually such as using circles or squares however I felt that this was too complex within the timeframe of the assessment. After researching other API’s such as the National Museum of Australia I found that the Atlas of Living Australia (ALA) had image URLs in their API. 

In my research I found that the Parsons School of Design have done interesting and engaging work with the Met museum. I was inspired by most of these projects. ("Parsons MS Data Visualization | The Met Museum | 2019", 2019)

To make the site more relevant to the user I decided to load information that is based on their current location. The ALA has about 94, 789, 163 occurrence records and 9, 024 datasets ("Home - Atlas of Living Australia", n.d.)  therefore I chose to pick a specific plant or animal species to show in my website. I accidently found a result about Australia’s frogs when using their website which inspired me to use frogs as a theme. ("Home - Atlas of Living Australia", n.d.) ("ALA API - how to access ALA web services", 2018)
\
\
\
One problem I encountered was how was I going to display all the results. To solve this, I found a stack overflow article which used a for loop for each item in an array/object, I used this to append the name and image to the page ("For loop through array and group every x number of items", 2014). I then researched into how to display the content in a grid so that multiple items could be viewed on one line and reduce the scrolling required. I followed a W3Schools responsive grid tutorial which used a flexbox style method of creating a 3-column grid which could be resized.  ("How To Create a Responsive Image Grid", n.d.)
\
\
\
At this stage I wanted to display more information if the user clicks on an item. I initially used the jQuery .click() event but I found that this would make all the items in the grid trigger at once. I needed a way for the site to know which item I was clicking and only display that items information. After researching various ways of using the .click() event I found a Stack Overflow post about clicking on an item and loading in dynamic data ("Click Event is not Working When Data loads Dynamic in jquery", 2018). In this post I found a solution that used the .on(‘click’) event which in my code looked like this:
```
$('body').on('click','{div name}' ,function() { 
    // My code in here
} 
```
I found that this worked when using “$(this).css()” to change the background colour it worked well. To show and hide text I applied a new class name called ‘hiddenText’ and the ‘display:none;’ property to hide it from view. I used the .find() method which allowed me to target the hidden text class and use the .toggle() method to change the visibility of the text. (".find() | jQuery API Documentation", n.d.) (".toggle() | jQuery API Documentation", n.d.)
\
\
\
During an in-class tutorial the tutor demonstrated the use of jQuery’s ‘getJson’ function to perform http GET requests to retrieve JSON data. Initially I was not going to transfer my code from the current fetch request that I was using. However, I was having issues related to images not loading consistently and I tested the code on the getJson I discovered that it retrieved the images more reliably. 
\
\
\
One issue I had was displaying placeholder or broken images. At first I used the ‘onerror = function()’ attribute to the image to solve the issue however I noticed that it didn’t work. After researching my issue further, I discovered a Stack Overflow post about how to use a placeholder image if the existing URL is not found (McCrossan, 2019). My solution targeted the image item and used an ‘.on(error)’ event to change the image source to a placeholder image. 
\
\
\
To add a personalised result to the page I wanted to add a button which would show frogs near the user. I used Google clouds reverse geocoding API and the navigator.geolocation API to get the users current location and address. ("Example of reverse geocoding", n.d.)

Initially I attempted to match the location of the user with the frogs recorded location then filtering it state however this resulted in only showing the first result ‘brown striped frog’. I realised that this was caused by how my program was formatted. I adjusted my code so that it used nested ‘.getJson’ requests which to fix the issue that variables were not declared in the main geolocation function.  
As I looked into the data of the URL “https://biocachews.ala.org.au/ws/occurrences/spatial*?q=frogs&pageSize=10”, I realised that it didn’t provide any results on frogs but returned results on birds. 

I then researched for a new API URL that would find information about frogs near the user’s latitude and longitude. I explored the biocache swagger documentation and ALA’s own web service API documentation however I could not find the API call that I needed ("Web service API", n.d.) ("biocache-service API", n.d.). I uncovered my API URL that I needed in the documenter.getpostman documentation which provided a URL which provided animal species near the user. I implemented this with the navigator.geolocation API’s latitude and longitude and changed the species to amphibians. ("ALA API's for GovHack 2020", 2020)
\
\
\
In the week 5 tutorial I was prompted to explore frog sounds and playing the sounds when the user clicks on the frog item. I began by checking if freesound.org had frog croaking’s as I already knew they had an API ("Resources — Freesound API documentation", n.d.). I found that the freesound API could only provide sound files for a limited selection of frogs. I decided that it would be more effective to download the frog audio files and load them in similar to Mitchl’s Drifter website which plays frog croaks along the Murrumbidgee river (Whitelaw, 2016).

When I was downloading the audio files from Amphibiaweb I noticed that the URL’s ended with “/family_names.wav”. I realised that instead of downloading the audio files I could link to these absolute URL’s instead (AmphibiaWeb, 2021.). An example of the Litoria Lesueurii’s audio file: 
“[https://amphibiaweb.org/sounds/Litoria_lesueurii.wav](https://amphibiaweb.org/sounds/Litoria_lesueurii.wav)”  
\
\
\
While researching how to change a space to an underscore in a title such as ‘litoria lesueurii’ to ‘litoria_lesueurii’ I looked in the JSON data for the best value to use and I spotted a property called ‘linkIdentifier’ which already had an underscore as a result I implemented this. 
I was unable to get the sounds play on the users click as the click function is outside of the scope of where the audio file is appended to the page. I attempted to implement using the audio play() method, $(‘audio’).play() and adding event listeners ("Play an audio file using jQuery when a button is clicked", 2011) ("HTML DOM Audio play() Method", n.d.). I was unable to solve this problem and used the html audio controls which allow the user to control the audio. 
\
\
\
To make my site mobile compatible I researched various CSS frameworks such as Foundation, Semantic UI and UIkit. I was unable to use a framework similar to Bootstrap which requires there to be a ‘container’, ‘row’ and ‘column’ as my program used the same class name for every item added to the page. I found that UIkit used a flexbox-styled layout similar to the current grid I was using and would allow me to keep the same class names for each item (Lazaris, 2019).

I used the card style layout as it would give a similar browsing experience on a mobile or desktop. I had to tweak the cards by adding class names such as ‘uk-grid-match’ which matches all the cards to the same height. While understanding how the framework works, I noticed there was animation effects such as ‘ScrollSpy’ which fades in the cards as the user scrolls down, which I implemented in my website. ("UIkit - Card", n.d.)
\
\
\
I finished the assignment by tweaking the hover effects on the cards to make it more obvious for the user that they are clickable. I also adjusted the copy around the number of sightings which have been recorded so that it was easier to understand.  ("Explore Your Area | Atlas of Living Australia", n.d.). I uploaded the final code to be viewed on GitHub Pages.
\
\
\
### Appendix B
#### Other Examples

During my research I found some other good examples of API project or API-like projects.  
("Codex Atlanticus", n.d.) 
("Apple of My Eyes", n.d.) 
("CeramicBeats", n.d.)
(Ran, n.d.)
And others from:
("Parsons MS Data Visualization | The Met Museum | 2019", 2019)

("Spotify: Listening Together", n.d.)
("Yesterday, Today, Tomorrow", n.d.)
("Pictoline - Timeline", n.d.)
(Weir & Wong, n.d.)
(Suzuki, n.d.)
("MetKids", n.d.)
("Cool stuff made with cultural heritage APIs", 2018)
\
\
\
### References for Appendixes 

.find() | jQuery API Documentation. Retrieved 20 March 2021, from https://api.jquery.com/find/

.toggle() | jQuery API Documentation. Retrieved 20 March 2021, from https://api.jquery.com/toggle/

ALA API - how to access ALA web services. (2018). Retrieved 19 March 2021, from https://support.ala.org.au/support/solutions/articles/6000196777-ala-api-how-to-access-ala-web-services

ALA API's for GovHack 2020. (2020). Retrieved 19 March 2021, from https://documenter.getpostman.com/view/12189774/T1Dwbtbd?version=latest#cd09fb97-05ce-480e-b47f-4b3c35417300

Apple of My Eyes. Retrieved 19 March 2021, from https://xingwei726.github.io/Major-Studio-1/Week10_InteractiveProject/test8/#page-1

AmphibiaWeb. 2021. Retrieved 20 March 2021, from https://amphibiaweb.org/lists/sound.shtml  University of California, Berkeley, CA, USA. 

biocache-service API. Retrieved 20 March 2021, from https://biocache.ala.org.au/ws/swagger-ui.html#/

CeramicBeats. Retrieved 19 March 2021, from https://azuic.github.io/CeramicBeats/

Click Event is not Working When Data loads Dynamic in jquery. (2018). Retrieved 20 March 2021, from https://stackoverflow.com/questions/29372003/click-event-is-not-working-when-data-loads-dynamic-in-jquery

Codex Atlanticus. Retrieved 19 March 2021, from https://www.codex-atlanticus.it/#/Overview

Cool stuff made with cultural heritage APIs. (2018). Retrieved 19 March 2021, from http://museum-API.pbworks.com/w/page/21933412/Cool%20stuff%20made%20with%20cultural%20heritage%20APIs

Example of reverse geocoding. Retrieved 19 March 2021, from https://developers.google.com/maps/documentation/geocoding/overview?csw=1#reverse-example

Explore Your Area | Atlas of Living Australia. Retrieved 19 March 2021, from https://biocache.ala.org.au/explore/your-area#-35.4540|149.0925|12|Amphibians

For loop through array and group every x number of items. (2014). Retrieved 19 March 2021, from https://www.sitepoint.com/community/t/for-loop-through-array-and-group-every-x-number-of-items/97966/2

Home -Atlas of Living Australia. Retrieved 20 March 2021, from https://www.ala.org.au/

How To Create a Responsive Image Grid. Retrieved 19 March 2021, from https://www.w3schools.com/howto/howto_css_image_grid_responsive.asp

HTML DOM Audio play() Method. Retrieved 20 March 2021, from https://www.w3schools.com/jsref/met_audio_play.asp

Intro into jQuery. [Image]. Retrieved from https://classroom.udacity.com/courses/ud245

Lazaris, L. (2019). 10 best CSS frameworks in 2020. Retrieved 19 March 2021, from https://www.creativebloq.com/features/best-css-frameworks

Marini, J. (2016). jQuery Essential Training [Video]. Retrieved from https://www.linkedin.com/learning/jquery-essential-training-2/welcome?u=2330002

McCrossan, R. (2019). Update img src if image does not exist. Retrieved 19 March 2021, from https://stackoverflow.com/questions/56166094/update-img-src-if-image-does-not-exist

MetKids. Retrieved 19 March 2021, from https://www.metmuseum.org/art/online-features/metkids/time-machine

Parsons MS Data Visualization | The Met Museum | 2019. (2019). Retrieved 19 March 2021, from https://parsons.nyc/met-museum-2019/

Pictoline - Timeline. Retrieved 19 March 2021, from https://www.pictoline.com/timeline

Play an audio file using jQuery when a button is clicked. (2018). Retrieved 20 March 2021, from https://stackoverflow.com/questions/8489710/play-an-audio-file-using-jquery-when-a-button-is-clicked

Ran, D. Buddhas at the Met. Retrieved 19 March 2021, from https://shuvitran.github.io/MajorStudio1/Project2-qualitative/FrontEnd/

Resources — Freesound API documentation. Retrieved 19 March 2021, from https://freesound.org/docs/api/resources_apiv2.html#sound-sound

Rocheleau, J. (2013). Code a Simple Github API Webapp using jQuery & Ajax. Retrieved 19 March 2021, from https://blog.teamtreehouse.com/code-a-simple-github-api-webapp-using-jquery-ajax

Spotify: Listening Together. Retrieved 19 March 2021, from https://listeningtogether.atspotify.com/

Suzuki, Y. Sound Of The Earth: The Pandemic Chapter. Retrieved 19 March 2021, from https://globalsound.dma.org/

UIkit - Card. Retrieved 19 March 2021, from https://getuikit.com/docs/card

Vieira, S. (2020). How To Use the JavaScript Fetch API to Get Data. Retrieved 19 March 2021, from https://www.digitalocean.com/community/tutorials/how-to-use-the-javascript-fetch-API-to-get-data

Web service API. Retrieved 19 March 2021, from https://api.ala.org.au/#

Weir, A., & Wong, R. The Museum of the World. Retrieved 19 March 2021, from https://britishmuseum.withgoogle.com/

Whitelaw, M. (2016). Drifter. Retrieved 19 March 2021, from https://mtchl.net/drifter/map.html 

Yesterday, Today, Tomorrow. Retrieved 19 March 2021, from https://yesterday.nfb.ca/

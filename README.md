# 11060 – Assessment 1 API Sketch
# Jehru Harris / U3202988

### Github Pages Url:
https://jehru.github.io/11060-Assessment-1/


### Reflection on development process

The full development process can be found in the Appendix A.  

I initially began this project with research, one topic I discovered was visualising cultural collections and displaying cultural data. In a ted talk by Mitchell Whitelaw (Whitelaw, 2010), he described how we should display and conserve our digital cultural data. Some of the key concepts that I learnt from this research was how as a designer you can change how people explore information on a web interface. And how our traditional models of searching for information don’t always work that way in the real world, for example in a museum you don’t go in looking for one specific item but rather want to explore what exists in a particular theme or topic. My takeaway is how as designers we should think how we display data in websites similar to the real world. (Whitelaw, 2010)

In my development process I found that choosing a theme helped to give the website structure and gave the website a consistent look and feel. 
I found that after working with several API’s the Geolocation API took some working out as the Google Cloud system requires you to toggle a button on/off to enable that feature from the URL. 
The Amphibaiweb’s audio files used an underscore between the species name in their audio URL’s so when I found the ‘link identifier’ data (which returned the species name with an underscore in between) in the Atlas of Living Australia (ALA) API this was very helpful as it reduced the coding required on switching a space to an underscore. This link identifier complimented the Amphibiaweb sound URL’s. 
Despite having to use a CSS framework that I am not familiar with I found the UI Kit framework to be easy to learn as their framework is well documented. I also found that it worked better than using a framework such as Bootstrap which would require me to add a row for each 3 or 4 items. UI Kit was easy to implement as all the frog cards had the same div classes. 

One of the major issues that I struggled with in this project was finding a good API. I felt that the API had to include images to make it visually engaging for the viewer. After finding the ALA API I discovered that it is not well documented despite this I found extra documentation which allowed me to create the functionality that was needed for the website. 
One other issue that I encountered was that every item that was appended to the page all used the same div tag and class name, this created issues with when the user clicked on one of items. It would trigger all the items in the page at once. This issue also persisted when images were not found the website would not return any images at all. I initially used the image=’onerror(function)’ which didn’t work but I found the jQuery method of .on(error) to work. I solved the on click problem by the .find() and toggle() method to toggle a hidden text class on the class item.

One of the main takeaways from this project was the importance of locating the right API for the project and that a well-documented API makes the development easier. I also learnt how to use jQuery to add and remove html items from a page. 
Prior to this project I had no previous knowledge of GLAM data and through this project I am now interested in taking GLAM data which traditionally (especially younger audiences) viewers may find uninteresting or disengaging and redesigning it to be explored with in a new and interesting way. 


### Design decisions 

The colour palette consists of a monochromatic green and a complimentary pink. 

![Colour Palette](/rationaleImages/colourPalette.png)
Format: ![Colour Palette for design, consisting of #d8f3dc, #298561, #095D42, #081C15, #df5979 ]
(Coolors - Colour Palette, n.d.)

All colours were tweaked colorsharks contrast tool. This tool gives advice to making your text and background colours WCAG 2.1 compatible. (Riggan, n.d.)
These colours were chosen with green as the primary colour as frogs are frog stereotypes are green, however at the end of the project I noticed that frogs near Canberra are usually more brown/grey in colour. The complimentary pink was chosen to contrast and stand out against the green. 
The UIKit cards were left as the default as I preferred the white and grey colours over my previous design which used a light green and dark green. I felt that the white looked more professional and contrasted better against the mint green background. 

The main function of the webpage is to display frogs that have been reported geographically near the user. The site has no additional pages to maintain simplicity and utilises a balanced symmetrical layout. The interface was designed to be user friendly easy for the user to navigate. 
The typeface chosen is Poppins, which was chosen due to its round friendly look. Poppins is an easy-to-read sans serif geometric typeface that gives the site a modern look. I wanted a friendly looking typeface to compliment the frogs that I was showcasing.  
I used a card style interface to show the frog images and information. This was implemented as it would provide a similar experience when using the site on the desktop or mobile. I was originally going to hide all the information behind the image and only show when the user clicks on it but felt that it was necessary to provide some information. 


### Examples of other relevant interfaces

The best 3 examples are shown here, more examples can be seen in the Appendix B.
I was inspired by the Apples at the Met, Ceramic Beats and Buddhas at the Met sites. All these websites are student projects and inspired me to build an interactive and engaging website.  

![Colour Palette](/assets/rationaleImages/colourPalette.png)
Format: ![Colour Palette for design, consisting of #d8f3dc, #298561, #095D42, #081C15, #df5979 ]
(Coolors - Colour Palette, n.d.)
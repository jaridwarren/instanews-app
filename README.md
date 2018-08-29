 # Instanews 'Top Stories' NYT App
 
 #### Author: Jarid Warren [ <jaridwarren@gmail.com> ]
 
 'Top Stories' application leveraging the [New York Times API](https://developer.nytimes.com/top_stories_v2.json) to dynamically generate the day's top news. Fully responsive design that reconfigures when a story-type is selected.
 
 ![alt text](./assets/images/demo.gif "Instanews")
 
 ## Motivation
 
 This project was used to practice using jQuery and `ajax()` to fetch JSON data and format it according to the design of the webpage. 
 
 ## Technology
 
 * JavaScript / jQuery
 * NPM / Gulp 
 * Sass / CSS
 
 ## Code Sample
 
 The following is how stories are dynamically appended to the DOM after fetching JSON data from the NYT.
 
 ```javascript
 $(".stories").append(
    `<a href="${data.results[key].url}" target="_blank" class="story-cell">
     <p class='story-text'>${data.results[key].abstract}</p></a>`
  );
  // set the background image of the new story
  $(".stories")
     .children(":last-child")
     .css("background-image",`url("${data.results[key].multimedia[4].url}")`);
```
## Installation:
Download or clone repo, then run the following commands in terminal:

`npm install` - to install gulp

`gulp sass` - to convert Sass files to CSS

`gulp scripts` - to call babel and uglify on JS files

`gulp browser-sync` - to refresh page and watch the build folder

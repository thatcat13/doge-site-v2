# CSS Week3 Solo SASS Project

### Building on a 2-day project this week, this is an alternate version of the dog magazine site. I'm using the same SASS tools created previously but implementing them in a new layout.

#### By _Cat Janowitz_

## Description

Doge-sit is an online magazine by dogs for dogs. This is version 2

## Thoughts and Feedback

This week I learned about SASS as a compiling tool that streamlines CSS design.  Using the 7-1 approach I practiced making folders of partials that contain modular rules, or chunks of rules, for every part of the website. SASS, operating under an import directive, "watches" and compiles all SASS-CSS (scss) code into a final output css file. The idea is to be able to re-use partials to build other sites. The efficiency comes from making changes in one location (partial files) rather than throughout the css code.

Some of the practices that I found useful included using a mixin to create a DIY grid and other components of the site (i.e., a card) that contains a universal list of style rules for that particular component. I used variables heavily (for color, card, intro, footer) with the idea in mind that I could re-use these variables for building other sites; it would be easy for me to change the style values in one place.

During the 2-day project Nathan and I found it challenging to fully utilize breakpoint variables. When including the breakpoint variables with other mixins (i.e., the grid mixin) the site wouldn't behave as expected. My guess is there was an overriding rule that we didn't pinpoint. Instead of using breakpoint variables we simply included media queries in the partial of that component.

I will change my approach today by checking for overriding rules when implementing mixins. I will follow the habit of my partner and use the inspector as much as I can since I feel I haven't used it as much as I could. My partner also showed me a nifty color palette tool called "Cooler" that I find worked really well for version 1.



## The Plan
| Term | Description | Implementation |
| :-------------     | :------------- | :------------- |
| **SASS partials** | Partials are .scss files containing code snippets that will be compiled into final CSS code. Uses the 7-1 file structure -- 7 folders with partials, 1 main.scss input file | Examples of how we're using partials include a folder that contains layout items specifically, nav, hero, intro, etc. Each file has element-specific styling |
| **grid system** | We will define column units much like Bootstrap (12 units per 1 row) and use SASS to calculate the space that each column takes up in that row. | Using a @for loop we will obtain SASS-calculated distribution of columns that are divisible by 12. This grid will afford uniformity and flexibility when used with breakpoints |
| **SASS @extend** | @extend is a SASS tool that allows you to share sets of CSS properties from one selector to another | We will use this for a clearfix on parent containers in our document; we will also use this to design various-sized cards and buttons |
| **SASS @mixin** | @mixin is a directive which allows you to reuse css rules through your site.| We will use @mixins for border radius, media queries and our responsive grid system to keep our code DRY. For example @mixin border-radius ($radius) {border-radius: $radius} (after you create this mixin you can you use it as a css declaration with @include border-radius(5px))|
|**SASS variables**| variables are a way to store information that you want to reuse throughout your stylesheet | We are going to use to hold many different values in our style sheet. For example: $primarycolor, $textcolor, $grid-columns: 12, $breakpoint-large: : "only screen and (min-width: 1000px)". |
| **SASS operators** | Operators allow us to do math in CSS. | We are using operators in our responsive grid (i.e., 100% / $grid-columns * index) |
| **Nesting** | SASS nesting places additional child selectors within parent selectors; it is a good way to organize CSS. | We are using nested selectors to style our nav |
| **@content** | @content is a sass directive that allows you to pass content block into the mixin. @content is equal to whatever you pass into the mixin inside of the curly braces | We are going to use the @content directive when we use the media query mixin to make elements responsive |
| **SASS loops** | @each is a control directive in the format of: @each $var in <list>. When processed, the parameter is applied to each item in the list. | We will be using @each loop  with a list of our color variables to apply styles to classes we create using the loop. |
| ** color functions ** | Built in SASS functions that allow color changes to be more fluid, easy, and complementary to the colors you're using; actions include darken and lighten, saturate and desaturate | We will use color functions to change the color in our nav list when hovering; we want that color to be a lighter version of the original color instead of a default color |


## Setup/Installation Requirements

* access computer with internet connection and a browser
* go to github.com and search "thatcat13"
* browse thatcat13's repositories to find 'product' repository
* click on 'doge-site-v2' repository and copy URL link that directs to this specific repository
* access computer terminal and make sure you are at the top directory
* in terminal, after $ prompt, type in: git clone {-don't type the following, just do the following: paste URL into terminal after git clone-} then hit enter
* complete 'doge-site-v2' repository should be available at top directory (although desktop is suggested)
* browse folder of repository to find 'index.html'; drag file directly into browser OR in browser click file open and access 'index.html'


* or access gh-pages assigned to this project:
* thatcat13.github.io/doge-site-v2

## Support and Contact Details
* For any questions please reach out to any of our team members below. Here are email and GitHub account details for each:

  * [Cat Janowitz](https://github.com/thatcat13) - thatcat13@gmail.com


## Technologies Used
* SASS
* CSS
* HTML


### License
* Font Awesome: License: SIL OFL 1.1



Copyright (c) 2017 **Cat Janowitz**

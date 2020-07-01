# Matthew Evans Portfolio site
This repository is used to contain my personal portfolio website. This portfolio site uses basic CSS, HTML and Javascript due to the limitations placed by using github pages. The site has been built to be modular allowing it easier to adjust content and styling.

Please click [here](https://mattie.io/) to view the portfolio site.


## 1. Contents 
* [Features](#2-features)
* [Setup and Configuration](#3-setup-and-configuration)
  * [HTML](#31-html)
  * [CSS](#32-css)
  * [JavaScript](#33-javascript)
* [Customization and Editing](#4-customization-and-editing)
  * [Header Section](#41-header-section)
     * [Background](411-background)
     * [Introduction](412-introduction)
     * [Navigation](413-navigation)
  * [Skills Section](#42-skills-section)
  * [Portfolio Section](#43-portfolio-section)
  * [Experience Section](#44-experience-section)
  * [Education Section](#45-education-section)
  * [Footer Section](#46-footer-section)
    * [Social Bar](#461-social-bar)
* [Changelog](#5-changelog)
* [Licence](#6-licence)

## 2. Features
* Fully responsive
* Code is in source control
* Code is commented appropriately
* HTML and CSS meet W3C validation standards
* Conforms to WCAG 2.1 AA standards
* Site is displayed within 2 seconds
* Site is served using HTTPS only
* Uses Google Analytics 
* Image optimisation
* Use of Variables for better theming changes 

## 3. Setup and Configuration
The site uses a basic design so that users can produce a portfolio site using the same template with minimal knowledge of HTML, CSS and Javascript. 

### 3.1. HTML 
The HTML contains all the content required for the site and with simple changes to text, images and hyperlinks a new user can use this template for a portfolio site.
Example of changes to be made:
Text:
```HTML
            <h1 class="section_title"> <strong>Matthew Evans</strong> </h1>
```
to
```HTML
            <h1 class="section_title"> <strong>NEW USER NAME</strong> </h1>
```
Images:
```HTML 
<img class="intro_image" src="https://secure.gravatar.com/avatar/d2cb1f7a860ed5505645c815cd294baf?s=2000" alt="a picture of Matthew Evans">
```
to 
```HTML
<img class="intro_image" src="/LOCATION/OF/MY/NEW/IMAGE" alt="a NEW PICTURE">
```
HyperLinks:
```HTML
<a href="https://github.com/M29992/M29992.github.io" class="btn">View project</a>
```
to
```HTML
<a href="https://github.com/NEWUSER/NEWPROJECT" class="btn">View project</a>
``` 

### 3.2. CSS 
The CSS can be fully adjusted and changed to create a completely different view and feel, however the site has been designed to allow users to quickly an easily change the theme by adjusting the following section within the style.CSS file : 
```CSS
    /* Variables for custom properties */
     :root {
        --font-primary: 'Raleway', sans-serif;
        --font-secondary: 'roboto';
        --font-weight-regular: 300;
        --font-weight-bold: 900;
        --font-primary-color: #Ffffff;
        --font-secondary-color: #D2D5DD;
        --accent-color: #9cdcfe;
        --body-line-height: 1.6;
        --heading-line-height: 1;
        --font-size-h1: 3rem;
        --font-size-h2: 2.25rem;
        --font-size-h3: 1.25rem;
        --font-size-h4: 1.15rem;
        --font-size-body: 1rem;
        --font-social-size: 1.75rem;
        --primary-color: #131920;
        --secondary-color: #1A222B;
        --box-shadow: 0.25em 0.25em 0.75em rgba(0, 0, 0, .25), 0.125em 0.125em 0.25em rgba(0, 0, 0, .15);
    }
    
    @media (min-width: 800px) {
         :root {
            --font-size-h1: 4.5rem;
            --font-size-h2: 3.25rem;
            --font-size-h3: 1.5rem;
            --font-size-body: 1.125rem;
            --font-social-size: 2.5rem;
        }
```
changing these setings allow Font, colours and sizes to be adjusted. 

The cover background contains a linear gradient and url that can be changed to adjust the secondary gradient colour and to change or remove the underlying background image.
```CSS
    /*cover background */
    
    .background {
        background-color: var(--primary-color);
        background-image: linear-gradient(to bottom, var(--primary-color), rgba(32, 50, 73, 0.825));
        background-size: cover;
        background-attachment: fixed;
        background-position: center;
    }
    
    @media(min-width:600px) {
        .background {
            background-color: var(--primary-color);
            background-image: linear-gradient(to bottom, var(--primary-color), rgba(32, 50, 73, 0.825)), url(../Images/Backgorunds/background.jpg);
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
        }
    }
 ```
 
### 3.3. Javascript 
Javascript has been used spariginly within the site design to limit compatibility issues and provide the smoothest operation. 

the hamburger.Js file is used to provide the behaviour for the navigation menu and should not need to be adjusted, it has 2 functions 
one to view the hidden navigation menu 
```Javascript
navToggle.addEventListener('click', () => {
    document.body.classList.toggle('nav-open');
});
```
the other is used to hide the navigation menu once a link is selected from within the menu.
```Javascript
navLinks.forEach(link => {
    link.addEventListener('click', () => {
        document.body.classList.remove('nav-open');
    })
})
```

There are additional scripts within the HTML document to gather the current year, use font awsome, and to get google analystics. 
    
## 4. Customization and Editing 
### 4.1. Header Section
The header section can be broken down to the following subsections: background, navigation and introduction.
#### 4.1.1. Background
The background section contains the headers initial background. 
Mobile view displays a CSS gradient from the primary colour to the skills section colour.
```CSS
background-image: linear-gradient(to bottom, var(--primary-color), rgba(32, 50, 73, 0.825));
```
Desktop view displays a background image under the CSS gradient that covers the full header section.
```CSS
background-image: linear-gradient(to bottom, var(--primary-color), rgba(32, 50, 73, 0.825)), url(../Images/Backgorunds/background.jpg);
```
#### 4.1.2. Introduction
The Introduction section consists of a title, an image and a subtitle.
The section title is centered and keeps a 1em padding at the bottom to give the title a level of importance and seperate the title from the image.
```CSS
.intro .section_title {
   position: relative;
   text-align: center;
   padding-bottom: 1em;
    }
```
The subtitle is centered and keeps a 1.5em padding at the top to give the image some space.
```CSS
.intro .section_subtitle {
   text-align: center;
   padding-top: 1.5em;
    }
```
The image when viewed on a desktop is displayed with a shadow and a maximum of 280 pixels in size, when viewed on a mobile device the image will take up 50% of the inline view.
```CSS
.intro_image {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
    border-radius: 0px 40px 0px 40px;
}
    
@media(min-width: 600px) {
   .intro_image {
      max-width: 280px;
      position: relative;
      z-index: 2;
      box-shadow: var(--box-shadow);
   }
} 
```

#### 4.1.3. Navigation 
  
### 4.2. Skills Section
The skills section uses a skill listcalled ```skills_list ``` and ```aSkill``` to show of users skills.
```skills_list ``` uses a CSS flexbox to dynamicaly add new ```aSkills``` to the right untill it hits the edge of the browser creating a new line for the next item. CSS styling to aligning items to the centre has been added to generate from the center out. 

```aSkill``` is used as a data item within ```skills_list ``` to represent a skill each ```aSkill``` object contains an image to represent the skill, a data hint to help with keyword search and scanning tools and an alt for accessibility.
```HTML
<div data-hint="Java" class="aSkill">
   <img src="Images/Skills/java.svg" alt="Java">
</div>
<!--close skill-->
```

### 4.3. Portfolio Section
Portfolio section displays a list of projects being worked on with a button to redirect to the project or code. 
projects are displayed as simple content held within a ```aProject``` div tag for desktop viewers ```aProjects``` are displayed as a grid given 400px per column in the grid. 
```HTML
<div class="aProject">
<h3>Mattie.io portfolio site</h3>
   <img src="Images/Projects/mattieio.png" alt="Mattie.io site views">
   <p>Portfolio site created for Mattie.io using HMTML, CSS and JavaScript. </p>
   <a href="https://github.com/M29992/M29992.github.io" class="btn">View project</a>
</div>
 <!--close a Project-->
```
   
### 4.4. Experience Section
Every job is held in a ```job``` object that contains the title, date, location and specs, these ```job``` objects are then contained within a ```experince_list```.
```CSS
.job {
        padding-top: 2em;
    }
    
    @media(min-width: 600px) {
        .job {
            max-width: 1600px;
            margin-right: auto;
            margin-left: auto;
            display: grid;
            grid-template-columns: 1fr 2fr 1fr;
            grid-template-rows: 1fr;
            grid-column-gap: 0px;
            grid-row-gap: 0px;
        }
        .overview {
            grid-column: 1/4;
            grid-row: 2;
        }
        .specs {
            grid-column: 1/4;
            grid-row: 3;
        }
    }
```
Each job has a padding of 2em from the previous job or section title. When viewing from a Desktop or display greater then 600 pixels the jobs are displayed using CSS grids to make use of the full width available. 

### 4.5. Education Section
Education works similarly to the education section, every certification or achievement is held in the ```education_list``` under a ```school``` object. 

A school object contains a level, date, location and specs.
```CSS
.school {
        padding-top: 2em;
    }
    
 @media(min-width: 600px) {
        .location {
            text-align: right;
        }
        .date {
            text-align: center;
        }
        .level {
            text-align: left;
        }
        .school {
            max-width: 1600px;
            margin-right: auto;
            margin-left: auto;
            display: grid;
            grid-template-columns: 1fr 2fr 1fr;
            grid-template-rows: 1fr;
            grid-column-gap: 0px;
            grid-row-gap: 0px;
        }
        .specs {
            grid-column: 1/4;
            grid-row: 3;
        }
    }
```
When viewing on a desktop or a device where its pixel width is greater then 600 pixels the content will be displayed within a grid layout using CSS grids to make use of the full width available.
  
### 4.6. Footer Section
The footer contains the social bar, the copywrite and a horizontal line.

Both the desktop view and mobile view use the same footer CSS. The copywrite is basic text that uses a simple javascript function to get the current year and display this on the site.
```Javascript
<script>
   document.write(new Date().getFullYear());
</script>
```

The horizontal line is used to break up the social media links from the copywrite information but can be better executed and will be adjusted in future builds to represent this.

#### 4.6.1 Social Bar
The social bar works similarly to all basic navigation CSS designs, each social media link is held in a div called ```social-list_item``` that is contained within the div social list.
All links within the footer first remove the styling, aligns the list to the centre and places the list in a CSS flexbox. Each social media link contains a link an aria-label for accessibility and a class that is ```fab fa-***``` where fab fa uses font awsome CSS (https://fontawesome.com/) to produce social media icons rather then using images or text.

```CSS
 .footer a {
        color: var(--font-secondary-color);
        font-size: var(--font-social-size);
        text-decoration: none;
    }
    
    .footer a:hover {
        color: var(--accent-color);
    }
    
    .social-list {
        list-style: none;
        display: flex;
        justify-content: center;
        margin: 0;
    }
    
    .social-list_item {
        margin: 0 .25em;
        padding: 0.2em;
    }
```
  

## 5. Changelog
### 1.0.4
* Draft write up of customization for site template added on ```readme```
### 1.0.3
* Social links and logo links adjusted to meet accessibility needs
### 1.0.2
* ```HTML``` adjusted to meet validation 
* ```CSS``` adjusted to meet validation
### 1.0.1
* Additonal comments created within ```CSS```, ```HTML```, ```JavaScript```
### 1.0.0
* Release and linked on social media 
### 0.1.1
* Content adjusted new profile picture added
### 0.1.0 
* changes to desktop view
* changes to mobile view 
### 0.0.2
* changes to desktop view 
### 0.0.1 
* Initial commits
* updated ```readme```

## 6. Licence
MIT License
See [```LICENSE.md```](LICENSE) for more information.

Copyright (c) 2020 Matthew Evans  

# Matthew Evans Portfolio site
This repository is used to contain my personal portfolio website. This portfolio site uses basic CSS, HTML and Javascript due to the limitations placed by using github pages. The site has been built to be modular allowing it easier to adjust content and styling.

Please click [here](https://mattie.io/) to view the portfolio site.


## 1. Contents 
* [Features](#2-features)
* [Setup and Configuration](#3-setup-and-configuration)
* [Customization and Editing](#4-customization-and-editing)
  * [Header Section](#41-header-section)
  * [Portfolio Section](#42-portfolio-section)
  * [Skills Section](#43-skills-section)
  * [Work Section](#44-work-section)
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
  

## 4. Customization and Editing 
### 4.1 Header Section
The header section can be broken down to the following subsections: background, navigation and introduction.
#### 4.1.1 Background
The background section contains the headers initial background. 
The mobile view displays a CSS gradient from the primary colour to the skills section colour.
The desktop view displays a background image under the CSS gradient that covers the full header section.
#### 4.1.2 Introduction
The Intro section consists of a title, an image and a subtitle.
the section title is centered and keeps a 1em padding at the bottom to give the title a level of importance and seperate the title from the image
the subtitle is also centered and keeps a 1.5em padding at the top to give the image some space
the image when viewed on a desktop screen is displayed with a shadow and a maximum of 280px in size when viewed on a mobile device the image will take up 50% of the inline view. the image is always central and the border radius curves 2 alternative corners.
#### 4.1.3 Navigation 
  
### 4.2 Skills Section
The skills section uses a skill list and askill to show of users skills.
the skills list uses a CSS flexbox to dynamicaly add new askills to the right untill it hits the edge of the browser creating a new line for the next item, aligning items to the centre so that items generate from the center out. 

askill is used as a data item within the skill list to represent a skill each askill contains an image to represent the skill, a data hint to help with keyword search and scanning tools and an alt for accessibility.

askill have margins on the left and right of 20px for mobile and 40px for desktop, each skill has an image attached to it to display an easy to distingush tool with a 5px padding around the images and a max width of 120px on mobile and 175px on desktop.

### 4.3 Portfolio Section
the portfolio section displays a list of projects being worked on with a button to redirect to the project or code. projects are displayed as siple content held within a aproject div tag for desktop viewers aProjects are displayed as a grid given 400px per column in the grid. 
   
### 4.4 Experience Section
  
### 4.5 Education Section
  
### 4.6 Footer Section
  
#### 4.6.1 Social Bar
  

## 5. Changelog
### 1.0.4
* Draft write up of customization for site template added on ```readme```
### 1.0.3
* Social links and logo links adjusted to meet accessibility needs
### 1.0.2
* HTML adjusted to meet validation 
* CSS adjusted to meet validation
### 1.0.1
* Additonal comments created within CSS, HTML, JavaScript
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

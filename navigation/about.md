---
layout: post
title: About
permalink: /about/
comments: true
---

## Where I have been

Here are some places I have lived.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";

    var living_in_the_world = [
        {flag: "0/01/Flag_of_California.svg", greeting: "Hello!", description: "California - all my life!!!"}, {flag: "8/88/Flag_of_India_%282-1%29.svg", greeting: "Namaste Beta", description: "India - where my parents are from"}

    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is where life has taken me!

**School**

- 🏫 Deer Canyon Elementary School(2015-2016)

- 🏫 Stone Ranch Elementary School(2016-2022)

- 🏫 Oak Valley Middle School(2022-2025)

- 🏫 Del Norte High School(Freshman year, 2025-Present)

**Extracurricular**

🛡️ 1 year of CyberPatriot

🎵 Traditional Indian vocal music since I was 5 years old

🎾 Used to play tennis

🏃 Started Cross Country this year

🥍 Currently in Lacrosse pre-season

💻 Helped my friend Matt with game developing in Roblox Studio

## Photo Gallery of my Interests

div class="grid-container" id="roblox_grid"></div>


<script>
   var robloxContainer = document.getElementById("roblox_grid");
  
   var projects = [
       {
           image: "{{site.baseurl}}/images/about/robloxs.jpeg",
           title: "dumb airport game",
           description: "My first project mainly made by myself made to be a chaos sandbox to parody normal airport games."
       },
       {
           image: "{{site.baseurl}}/images/about/miami.webp",
           title: "Tacitorn Port Game",
           description: "An attempted project to make a GTA Clone. Well-developed with lots of code but nowhere close to finished currently not being maintained. Major improvement to dumb airport game."
       },
       {
           image: "{{site.baseurl}}/images/about/zombie.webp",
           title: "Left With Nothing",
           description: "My current project. It's a zombie survival game where your put into an abandoned city forced to scavenge for weapons to survive the  and their variants, hostile NPCs, and other players. My most well-developed game compared to my previous ones. "
       }
   ];


   for (const project of projects) {
       var gridItem = document.createElement("div");
       gridItem.className = "grid-item";


       var img = document.createElement("img");
       img.src = project.image;
       img.alt = project.title;


       var title = document.createElement("p");
       title.textContent = project.title;


       var description = document.createElement("p");
       description.textContent = project.description;


       gridItem.appendChild(img);
       gridItem.appendChild(title);
       gridItem.appendChild(description);
       robloxContainer.appendChild(gridItem);
   }
</script>



### Background

My family is my main inspiration, and they are the reason I am still here today and in this CS class!

👩🏻 1 older sister in college

🇮🇳 Both parents from India, more specifically southern region, with my dad being from Karnataka and my mom being from Tamil Nadu

👨‍👩‍👦 My cousins are more on my dad's side, and a lot of them live in India, but 2 of them live in the US and one of them lives in the UK


<comment>
Gallery of Pics...
</comment>
<div class="image-gallery">
  <img src="" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/mort2.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/mort4.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/mort5.jpg" alt="Image 3">
</div>

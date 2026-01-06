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

## Photo Gallery of my interests

// Setup: lines from here to "Copy"
<div id="grid_container"></div>

<script>
var outputElement = document.getElementById("grid_container");

// ⬇️ Copy Start: start on outputElement.innerHTML line 
// Clear the output
outputElement.innerHTML = '';

// Define the data array of flagobjects
const living_in_the_world = [
  {
    flag: "https://upload.wikimedia.org/wikipedia/commons/0/01/Flag_of_California.svg",
    greeting: "Hey",
    description: "California - forever"
  },
  {
    flag: "https://upload.wikimedia.org/wikipedia/commons/b/b9/Flag_of_Oregon.svg",
    greeting: "Hi",
    description: "Oregon - 9 years"
  },
  {
    flag: "https://upload.wikimedia.org/wikipedia/commons/b/be/Flag_of_England.svg",
    greeting: "Alright mate",
    description: "England - 2 years"
  },
  {
    flag: "https://upload.wikimedia.org/wikipedia/commons/e/ef/Flag_of_Hawaii.svg",
    greeting: "Aloha",
    description: "Hawaii - 2 years"
  }
];

// Create a pre container with id
const container = document.createElement('pre');
container.id = 'grid_container';

/// Style the container for JSON display 
container.style.border = '2px dashed';
container.style.padding = '10px';
container.style.borderRadius = '8px';
container.style.overflow = 'auto';

// Add the Flag data as JSON text 
container.textContent = JSON.stringify(living_in_the_world, null, 2);

// Add containter to output 
outputElement.appendChild(container);

... All ui runner code from Step 4 here
outputElement.appendChild(container);
// ⬆️ Copy End: end on outputElement.appendChild line


// Setup: be sure to include end script tag
</script>

<style>
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
### Background

My family is my main inspiration, and they are the reason I am still here today and in this CS class!

👩🏻 1 older sister in college

🇮🇳 Both parents from India, more specifically southern region, with my dad being from Karnataka and my mom being from Tamil Nadu

👨‍👩‍👦 My cousins are more on my dad's side, and a lot of them live in India, but 2 of them live in the US and one of them lives in the UK


<comment>
Gallery of Pics...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/mort1.jpg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/mort2.jpg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/mort4.jpg" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/mort5.jpg" alt="Image 3">
</div>

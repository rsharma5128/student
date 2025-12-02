---
layout: post
title: About
permalink: /about/
comments: true
---

## Where I have been



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

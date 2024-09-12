---
layout: page
title: Active & Fitness
permalink: /traveling/active/
---

<style>
    .container {
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
        width: 100%;
        font-size: small;
        font-family: Georgia, 'Times New Roman', Times, serif;
        margin-top: 150px;
        margin-bottom: 50px;
        padding: 20px;
        box-sizing: border-box;
    }

    .item {
        display: flex;
        flex-direction: row; 
        gap: 20px;
        align-items: center;
        width: 100%;
        max-width: 600px; 
    }

    .item img {
        width: 150px; 
        height: auto;
        border-radius: 5px; 
    }

    .text-container {
        display: flex;
        flex-direction: column; 
        max-width: 400px;
    }

    .title {
        font-weight: bold;
        font-size: medium;
    }

    .description {
        font-size: small;
    }

    .location {
        font-size: small;
    }
</style>

<div class="container" id="container">

</div>

<script>
    var container = document.getElementById("container");
    const places = [
        {
            "link": "3b1a18a6-e174-4868-93c9-1e3232efb534", 
            "title":"Rio De Janeiro Helicopter Flight Tour", "description": "Rio De Janeiro Helicopter Flight Tour will allow the tourist to see the wonders of Rio in a short, fast, and unforgettable journey.", 
            "locationLink": "/traveling/nature/rio/"
        },
    ];

    for (let i = 0; i < places.length; i++) {
        var item = document.createElement("div");
        item.classList.add("item");

        var img = document.createElement("img");
        img.src = "https://github.com/user-attachments/assets/" + places[i].link;

        var textContainer = document.createElement("div");
        textContainer.classList.add("text-container");

        var title = document.createElement("div");
        title.classList.add("title");
        title.textContent = places[i].title;

        var desc = document.createElement("div");
        desc.classList.add("description");
        desc.textContent = places[i].description;

        textContainer.appendChild(title);
        textContainer.appendChild(desc);

        item.appendChild(img);
        item.appendChild(textContainer);
        container.appendChild(item);

    
       // location link

        var country = places[i].locationLink.split("/").filter(Boolean).pop();
        country = country.charAt(0).toUpperCase() + country.slice(1);
        var locationLink = document.createElement("div");
        locationLink.classList.add("location");
        locationLink.innerHTML = `<a href="{{ site.baseurl }}${places[i].locationLink}">More about ${country}</a>`;
        textContainer.appendChild(locationLink);
        
    }
</script>

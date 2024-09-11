---
layout: page
title: Nature
permalink: /nature/
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
        flex-direction: row; /* Image and title/description side by side */
        gap: 20px;
        align-items: center;
        width: 100%;
        max-width: 600px; /* Adjust this for desired width */
    }

    .item img {
        width: 150px; /* Set the image width */
        height: auto;
        border-radius: 5px; /* Optional styling for images */
    }

    .text-container {
        display: flex;
        flex-direction: column; /* Stack title on top of description */
        max-width: 400px;
    }

    .title {
        font-weight: bold;
        font-size: medium;
    }

    .description {
        font-size: small;
    }
</style>

<div class="container" id="container">
    
</div>

<script>
    var container = document.getElementById("container");
    const places = [
        {"link": "acd0f0dc-338b-4ba3-a825-2bb3d7ae5a00", "title":"Serene Forest", "description": "A serene view of the forest."},
        {"link": "ec644c2d-91e0-4cf0-aff8-639bc2e29f23", "title":"Hanauma Bay Nature Preserve", "description": "A tranquil lake at sunset."},
        {"link": "f711d891-b4bd-40e6-a59a-2cc49858c017", "title":"Snowy Peaks", "description": "A mountain range with snowy peaks."},
        {"link": "6130dc07-f803-4acf-97f6-eec3b4f47acf", "title":"Flowing River", "description": "A flowing river surrounded by trees."},
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
    }
</script>

---
layout: page
title: Nature
permalink: /traveling/nature/
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
            "link": "444b80e0-3900-47e9-91f6-c4f175aec29d", 
            "title":"Hanauma Bay Nature Preserve, Hawaii", 
            "description": "This protected marine life conservation area, named after its unique curved bay, is a popular snorkeling spot in Hawaii. Formed within a volcanic cone on the eastern side of Oahu, this marine sanctuary is home to vibrant marine life and well-preserved corals.", 
            "locationLink": "/traveling/nature/hawaii/"
        },

        {
            "link": "40f11f77-5461-4a51-83d0-f6e6fa30b335", 
            "title":"Sian Ka'an Biosphere Reserve, Yucatan Peninsula", 
            "description": "The Sian Ka'an Biosphere Reserve is a biosphere reserve in Tulum Municipality in the Mexican state of Quintana Roo. The reserve features a mosaic of ecosystems, including coastal dunes, mangroves, and marshes, and its interconnectedness is vital for the health of the region.", 
            "locationLink": "/traveling/nature/yucatan/"
        },
        
        {
            "link": "c4971f0b-c8a4-457c-ba80-3c266823c663", 
            "title":"Santorini Caldera, Greece", 
            "description": "Santorini caldera is a large, mostly submerged caldera, located in the southern Aegean Sea. Its large, water-filled volcanic crater is a defining geological feature of the island and is surrounded by the steep cliffs and picturesque villages that Santorini is famous for.", 
            "locationLink": "/traveling/nature/greece/"
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

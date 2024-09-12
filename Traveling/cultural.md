---
layout: page
title: Cultural & Historic
permalink: /traveling/cultural/
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
            "link": "b0650662-02da-46cb-968a-aebfedfb079b", 
            "title":"Fez to Marrakech 3 days Sahara Desert tour, Fez", 
            "description": "The best way to make your way between the imperial cities of Fez and Marrakech is to get out into the Moroccan landscape and experience the Sahara Desert on this three-day tour. Camel rides, desert camp, riad accommodation and transport will all be covered, so you can just enjoy your desert holiday.", 
            "locationLink": "/traveling/fez/"
        },

        {
            "link": "eb622241-0564-442e-b5d1-51bf523f9a24", 
            "title":"Mosque of Muhammad Ali, Cairo", 
            "description": "Located in the Citadel, this mosque was built between 1824 and 1857 in the Ottoman style by Mohammad Ali Pasha, a ruler of Egypt.", 
            "locationLink": "/traveling/cairo/"
        },
        
        {
            "link": "e4759b50-212a-465c-9bf8-1338d822c0f0", 
            "title":"Old City of Jerusalem, Jersalem", 
            "description": "Characterized by narrow, winding streets and alleyways, this ancient part of the city is filled with shrines and attractions holy to Jews, Christians and Muslims including the Western Wall, Temple Mount and the Church of the Holy Sepulchre.", 
            "locationLink": "/traveling/jerusalem/"
        },
        {
            "link": "772bb3fe-1f29-4034-8c84-c73fa5fc9e98", 
            "title":"Cathédrale Notre-Dame de Paris, Paris", 
            "description": "The iconic Notre Dame Cathedral Paris—meaning ‘Our Lady of Paris’—is a masterpiece of French Gothic architecture. Built back in the 12th century, the important monument has witnessed many historical events. ", 
            "locationLink": "/traveling/paris/"
        },
        {
            "link": "c5bedd50-f263-43ca-aa93-a14f6fa948e2", 
            "title":"Buckingham Palace, London", 
            "description": "Buckingham Palace is recognised around the world as the focus of national and royal celebrations as well as the backdrop to the regular Changing the Guard ceremony. Explore the magnificent State Rooms which are open to visitors for 10 weeks each summer and on selected dates during winter and spring.", 
            "locationLink": "/traveling/london/"
        },
        {
            "link": "6785d497-96f6-4889-8a16-db31361a6f24", 
            "title":"Yasukuni Shrine, Tokyo", 
            "description": "A large, torii gate stands at the entrance to this shrine built in memory of those who lost their lives defending Japan. Many officials still come and offer prayer annually on August 15, the anniversary of Japan's defeat in World War II.", 
            "locationLink": "/traveling/tokyo/"
        },
        {
            "link": "f5046420-ec58-4de1-8b8f-d4b21a528186", 
            "title":"Jing'an Temple, Shanghai", 
            "description": "The Jing'an Temple in Shanghai, China is a Buddhist temple with a rich history and many notable features. The temple has multiple halls and courtyards, including the main hall, the entrance hall, and the Guanyin Hall. It also features a pagoda, a large bronze bell, and several notable Buddha statues.", 
            "locationLink": "/traveling/shanghai/"
        },
        {
            "link": "e4759b50-212a-465c-9bf8-1338d822c0f0", 
            "title":"9/11 Memorial & Museum, New York City", 
            "description": "Through commemoration, exhibitions and educational programs, The National September 11 Memorial & Museum, a nonprofit in New York City, remembers and honors the 2,983 people killed in the horrific attacks of September 11, 2001.", 
            "locationLink": "/traveling/nyc/"
        },
        {
            "link": "5423fb83-f220-4b9a-8dd0-5235c013c5e7", 
            "title":"Shri Krishna Temple, Bahrain", 
            "description": "This 200-year-old temple located near the Bab-al-Bahrain is a beautiful jewel tucked away in between the market area in Bahrain. The design of the temple is colorful and mimics several Rajasthani elements. A perfect place to offer prayers in the busy city life, the temple also hosts several functions and a daily morning prayer.", 
            "locationLink": "/traveling/bahrain/"
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

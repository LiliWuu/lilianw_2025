---
layout: page
title: Family-Friendly
permalink: /traveling/fam/
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
            "link": "62615a22-44de-4640-a970-0bea99aa9b2e", 
            "title":"Baga Beach, Goa", "description": "Baga Beach is a popular beach and tourist destination in North Goa. Baga is located at the north end of the contiguous beach stretch that starts from Sinquerim, Candolim, leads to Calangute, and then to Baga. The beach contains rows of shacks and fishing boats, and at high tide the beach is narrow.", 
            "locationLink": "/traveling/goa/"
        },
        {
            "link": "30ae40e3-ed0e-4f3d-bbc2-73440b620188", 
            "title":"Playa Mujeres Waterpark, Cancun", "description": "Dreams Playa Mujeres features 65,000 square feet of inviting swimming pools, an on-site water park, live entertainment, world-class golf greens, soothing spas, oversized luxurious suites, and an incredible interactive Dolphin Habitat.", 
            "locationLink": "/traveling/cancun/"
        },
        {
            "link": "4b07416a-3a40-4f69-9b43-bf8f5bf9ea83", 
            "title":"Bellagio Conservatory & Botanical Garden, Las Vegas", "description": "Skylit Bellagio atrium featuring vibrant, seasonal scenes composed of plants, flowers & trees. Each season, the enormously talented Horticulture and Engineering teams transform the 14,000-square-foot Botanical Gardens into a showcase of inspiring sights, sounds, scents and colors. Spring, Summer, Fall and Winter are all featured—along with a special display for Lunar New Year. When the seasons change so do the displays.", 
            "locationLink": "/traveling/lasvegas/"
        },
        {
            "link": "aba76e5d-ab78-41de-ad2b-cf723dfaac8d", 
            "title":"Musical Instrument Museum, Phoenix", "description": "The World's Only Global Musical Instrument Museum. Home of the MIM Music Theater--a 300-seat acoustically superb performance space--as well as the award-winning Café Allegro (open 11 am - 2 pm daily) and the MIM Museum Store.", 
            "locationLink": "/traveling/phoenix/"
        },
        {
            "link": "d8fcca8d-d82d-4ab0-9a8a-55fcea3523e7", 
            "title":"Klong Tour Thonburi, Bangkok", "description": "Get a firsthand look at the scenic life along Bangkok’s waterways during a 4-hour tour by long-tail boat. You'll journey down the legendary Chao Phraya River and cruise along the tributary canals, or 'khlongs,' of Thonburi. You have the option to upgrade to a boat tour for your private party. Transport is included from downtown hotels,",
            "locationLink": "/traveling/bangkok/"
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


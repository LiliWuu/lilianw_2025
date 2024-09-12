---
layout: page
title: About
description: About Me
permalink: /about/
---

<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        max-width: 700px; 
        height: auto; 
        color: #ab9fd1;
        font-family: serif;
        font-size: 18px;
        line-height: 1.5;
        margin: 50px; 
        padding: 20px;
        border-radius: 10px; 
    }

    .image-container {
        display: inline-block;
        padding: 10px;
        border-radius: 30px;
        background: linear-gradient(270deg, #30e8b9, #e830a8, #82f186, #309de8, #e83030);
        background-size: 1000% 1000%;
        -webkit-animation: AnimationName 31s ease infinite;
        -moz-animation: AnimationName 31s ease infinite;
        animation: AnimationName 31s ease infinite;
        position: relative;
        margin-bottom: 40px;
    }

    @-webkit-keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }
    @-moz-keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }
    @keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }

    .image {
        display: block;
        border-radius: 24px;
        width: 420px;
        height: 400px;
    }

    /* flags */
        .grid-container {
            display: flex;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); gap: 200px;
            align-items: center;
            position: relative;
            width: 100%;
            height: 200px;
            font-size: small;
            font-family: Georgia, 'Times New Roman', Times, serif;
            margin: 100px;
        }
        .img {
            object-fit: contain;
        }

    #socials {
        display: flex;
        justify-content: center; 
        align-items: center;  
        gap: 20px; 
        background-color: #ad9ede;
        width: 100%; 
        height: 60px;
        opacity: 0.6;
        margin-top: 20px;
        padding: 10px 0;
    }

    #socials img {
        width: 50px;  
        height: 50px;  
        vertical-align: middle;  
    }

    /* image gallery */
    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        color: #ab9fd1;
        font-family: Georgia, 'Times New Roman', Times, serif;
        margin-top: 50px;
        padding: 20px;
    }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;

    }

    .scroll-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        margin-top: 20px;
    }

    .scroll-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }

    .click {
        cursor: pointer;
    }
</style>

<div class="container">
    <div class="grid-container" id="grid-container"></div>
    <div class="image-container">
        <img id="image" src="../images/IMG_5299.png" alt="Me and my friend" class="image">
    </div> 
    <p>
    Hi! My name is Lilian Wu and I'm currently a junior in Del Norte High School. I took CSSE last year and am now taking CSA to gain a deeper understanding about Java. In my free time, I enjoy playing tennis, playing piano, playing with my cats, cooking, and improving my skill set. I'm passionate about STEM and look forward to pursuing a career in this field, as I love learning and solving problems.</p>
</div> 

## My Values

<div class="image-gallery">
    <figure>
        <img src="../images/fam.jpg" alt="fam+friends" class="click" id="family">
        <figcaption>Family & Friends</figcaption>
    </figure>
    <figure>
        <img src="../images/hobbies.jpg" alt="hobbies" class="click" id="hobbies">
        <figcaption>Hobbies</figcaption>
    </figure>
    <figure>
        <img src="../images/cultural.jpg" alt="culture" class="click" id="culture">
        <figcaption>Culture</figcaption>
    </figure>
</div>
<div class="scroll-gallery" id="scroll-gallery"></div>

<div id="socials">
        <a href="https://github.com/LiliWuu"><img src="../images/git.png"></a>
        <a href="https://www.instagram.com/lilianw.w/"><img src="../images/instagram.png"></a>
        <a href="https://www.youtube.com/@lilianw6836"><img src="../images/youtube.png"></a>
</div>

<script>
    var grid_container = document.getElementById("grid-container");

    const flags = [
        {"flag": "Chinese Flag", "Time Spent":"5 years", "Description": "I was born in the San Jose but moved to Beijing when I was two years old."},
        {"flag": "Californian Flag", "Time Spent": "9 years", "Description": "My family and I moved to San Diego because of my dad's work."},
    ];

    for (const flag of flags) {
        var gridItem = document.createElement("div");
        var img = document.createElement("img");
        if (flag.flag == "Chinese Flag") {
         img.src = "https://upload.wikimedia.org/wikipedia/commons/f/fa/Flag_of_the_People%27s_Republic_of_China.svg";
        } else {
            img.src = "https://upload.wikimedia.org/wikipedia/commons/0/01/Flag_of_California.svg";
        }
        
        var desc = document.createElement("p");
        desc.innerText = flag["Time Spent"] + "\n" + flag.Description;

        
        grid_container.appendChild(gridItem);
        gridItem.appendChild(img);
        gridItem.appendChild(desc);
    }

    //img gallery

    const gallery_images = {
        family: [
            "../images/gallery/1.1.jpg",
            "../images/gallery/1.2.jpg",
            "../images/gallery/1.3.jpg",
            "../images/gallery/1.4.jpg",
            "../images/gallery/1.5.jpg",
            "../images/gallery/1.6.jpg",
            "../images/gallery/1.7.jpg",
            "../images/gallery/1.8.jpg",
            "../images/gallery/1.9.jpg",
            "../images/gallery/1.10.jpg",
            "../images/gallery/1.11.jpg",
            "../images/gallery/1.12.jpg",
            "../images/gallery/1.13.jpg",
            "../images/gallery/1.14.jpg",
            "../images/gallery/1.15.jpg",
            "../images/gallery/1.16.jpg",
            "../images/gallery/1.17.jpg",
        ],
        hobbies: [
            "../images/gallery/2.1.jpg",
            "../images/gallery/2.2.jpg",
            "../images/gallery/2.3.jpg",
            "../images/gallery/2.4.jpg",
            "../images/gallery/2.5.jpg",
            "../images/gallery/2.6.jpg",
            "../images/gallery/2.7.jpg",
            "../images/gallery/2.8.jpg",
            "../images/gallery/2.9.jpg",
            "../images/gallery/2.10.jpg",
            "../images/gallery/2.11.jpg",
        ],
        culture: [
            "../images/gallery/3.1.jpg",
            "../images/gallery/3.2.jpg",
            "../images/gallery/3.3.jpg",
            "../images/gallery/3.4.jpg",
            "../images/gallery/3.5.jpg",
            "../images/gallery/3.6.jpg",
            "../images/gallery/3.7.jpg",
            "../images/gallery/3.8.jpg",
            "../images/gallery/3.9.jpg",
            "../images/gallery/3.10.jpg",
            "../images/gallery/3.11.jpg",
            "../images/gallery/3.12.jpg",
        ]
    };

    const gallery_descriptions = {
    family: [
        "👨‍👩‍👧‍👦 I have a family of four",
        "🐱 I own four cats even though I'm allergic to them",
        "✈️ My family likes to travel",
        "👭 I'm been with some of my friends since elementary school"
    ],
    hobbies: [
        "🎹 I started playing the piano when I was seven",
        "🎾 I've been playing tennis for two years, ever since I quit swimming",
        "🍰 In my free time I like to bake (and cook)",
    ],
    culture: [
        "🌶️ I like spicy food, and my favorite chinese dish is Huigou Rou",
        "🇨🇳 My family likes to travel to China",
        "🏛️ My favorite part of China is the food, the historical sites, and the way of living",
    ]
};

    function loadGallery(category) {
    var scroll_gallery = document.getElementById("scroll-gallery");
    scroll_gallery.innerHTML = ''; 

    var existingDescContainer = document.querySelector(".desc-container");
    if (existingDescContainer) {
        existingDescContainer.remove();
    }
    var images = gallery_images[category]; 
    var descriptions = gallery_descriptions[category]; 

    var descList = document.createElement("ul");

    for (let i = 0; i < images.length; i++) {
        var image = document.createElement("img");
        image.src = images[i];
        scroll_gallery.appendChild(image);
    }

    var descContainer = document.createElement("div");
    descContainer.className = "desc-container"; 
    for (let i = 0; i < descriptions.length; i++) {
        
        var listItem = document.createElement("li");
        listItem.innerText = descriptions[i] || "Description not available"; 
        descList.appendChild(listItem);
    }

    descContainer.appendChild(descList);
    scroll_gallery.parentNode.appendChild(descContainer);
}


// Adding event listeners for the category buttons
document.querySelectorAll(".click").forEach(item => {
    item.addEventListener("click", function() {
        loadGallery(this.id); // Load the gallery based on the clicked category
    });
});

</script>

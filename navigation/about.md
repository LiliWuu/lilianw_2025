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
        width: 700px;
        height: 800px;
        position: relative;
        color: #ece6ff;
        padding: 20px;
        font-family: serif;
        font-size: 18px;
        line-height: 50px;
        padding-top: 300px;
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
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */gap: 50px;
            align-items: center;
            position: relative;
            width: 500px;
            height: 200px;
            font-size: small;
            font-family: Georgia, 'Times New Roman', Times, serif;
            margin: 100px;
          }
        .gridItem {
            text-align: center;
        }
        .img {
            object-fit: contain;
        }
        .p {

            margin: 2px 0;
        }

    #socials {
        display: flex;
        background-color: #ad9ede;
        width: 435px;
        height: 50px;
        margin: 10px;
        position: relative;
        opacity: 0.6;
        justify-content: center;
        align-items: center;
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
    }

</style>

<div class="container">
    <div class="grid-container" id="grid-container"></div>
    <div class="image-container">
        <img id="image" src="../images/IMG_5299.png" alt="Me and my friend" class="image">
    </div> 
    <p>Hi! My name is Lilian Wu and I'm currently a junior in Del Norte High School. I took CSSE last year and am now taking CSA to gain a deeper understanding about Java. In my free time, I enjoy playing tennis, playing piano, playing with my cats, cooking, and improving my skill set. I'm passionate about STEM and look forward to pursuing a career in this field, as I love learning and solving problems.</p>

    <div id="socials">
        <p><a href="https://github.com/LiliWuu"><img src="../images/github.png" width="50" height="50"></a></p>
        <p><a href="https://www.instagram.com/lilianw.w/"><img src="../images/instagram.png" width="50" height="40"></a></p>
        <p><a href="https://www.youtube.com/@lilianw6836"><img src="../images/youtube.png" width="40" height="50"></a></p>
    </div>
</div> 





<div class="image-gallery">

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
</script>

---
layout: page
title: Nature
permalink: /nature/
---

<!-- test -->

<style>
        .container {
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




</style>

<div class="container" id="container">
    
</div>

<script>
    var container = document.getElementById("container");
    const places = [
        {"link": "acd0f0dc-338b-4ba3-a825-2bb3d7ae5a00"},
        {"link": "ec644c2d-91e0-4cf0-aff8-639bc2e29f23"},
        {"link": "f711d891-b4bd-40e6-a59a-2cc49858c017"},
        {"link": "6130dc07-f803-4acf-97f6-eec3b4f47acf"},
    ];

    for (let i = 0; i < places.length; i++) {
        var img = document.createElement("img");
        img.src = "https://github.com/user-attachments/assets/" + places[i].link;
        container.appendChild(img);
    }

    

</script>
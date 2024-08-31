---
layout: page
title: About
permalink: /about/
---

<style>
    .container {
        width: 700px;
        height: 800px;
        background-color: #ad9ede;
        margin: 0 auto;
        position: relative;
        right: -400px;
        top: 100px;
        color: #ece6ff;
        padding: 20px;
        font-family: serif;
        font-size: 18px;
        line-height: 50px;
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
        top: -300px;
        left: -285px;
        transform: translateX(-50%);
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

    #socials {
        display: flex;
        background-color: #ad9ede;
        width: 435px;
        height: 50px;
        margin: 10px;
        position: relative;
        top: -300px;
        left: -30px;
        opacity: 0.6;
        justify-content: center;
        align-items: center;
    }
</style>

<div class="container">
    <p>Hi! My name is Lilian Wu and I'm currently a junior in Del Norte High School. I took CSSE last year and am now taking CSA to gain a deeper understanding about Java. In my free time, I enjoy playing tennis, playing piano, playing with my cats, cooking, and improving my skill set. I'm passionate about STEM and look forward to pursuing a career in this field, as I love learning and solving problems.</p>

    <div class="image-container">
        <img id="image" src="../images/IMG_5299.png" alt="Me and my friend" class="image">
    </div> 
</div> 

<div id="socials">
    <p style="position: absolute; left: 125px; top: -10%;"><a href="https://github.com/LiliWuu"><img src="../images/github.png" width="50" height="50"></a></p>
    <p><a href="https://www.instagram.com/lilianw.w/"><img src="../images/instagram.png" width="50" height="40"></a></p>
    <p><a href="https://www.youtube.com/@lilianw6836"><img src="../images/youtube.png" width="40" height="50"></a></p>
</div>
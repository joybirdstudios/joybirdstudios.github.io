---
layout: post
title: "PEARL JAM: DARK MATTER WORLD TOUR 2024"
author: "Deana Seitz and Aster Teter"
categories: music videos
tags: [music videos, color grading, editing, visuals]
image: pjdm-header.jpg
---
---
layout: post
author: "Deana Seitz and Aster Teter"
title: "Pearl Jam: Dark Matter World Tour 2024"
categories: music videos
tags: [music videos, color grading, editing, visuals]
image: pjdm-header.jpg
---
<link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css?family=Raleway|Rozha+One|Montserrat:400,500,600,700&display=swap" rel="stylesheet">

<style>
/* Import Montserrat for all paragraph text */
.post-content p {
    font-family: 'Montserrat', sans-serif !important;
}

/* Force Montserrat on all regular paragraphs */
p:not([class*="anim-title-line"]):not([style*="color: grey"]) {
    font-family: 'Montserrat', sans-serif !important;
}

/* Gallery Styles */
.gallery-container {
    --gallery-primary-color: #fff;
    --gallery-secondary-color: rgba(0, 0, 0, 0.9);
    --gallery-transition-duration: 0.5s;
    margin-bottom: -5px;
    font-family: 'Montserrat', sans-serif;
    background: #fff;
}

.gallery-container .container {
    width: 100% !important;
    margin: 0 auto;
    overflow: hidden;
}

/* Use flexbox for horizontal stacking */
.gallery-container .fx2 {
    display: flex !important;
    flex-direction: row !important;
    flex-wrap: nowrap !important;
    justify-content: space-between !important;
    align-items: stretch !important;
    width: 100% !important;
    gap: 1px !important;
}

.gallery-container .col4 {
    flex: 1 !important;
    min-width: 0 !important; /* Allow flex items to shrink */
    position: relative;
    box-sizing: border-box;
}

.gallery-container .transition {
    transition: all var(--gallery-transition-duration) ease;
}

.gallery-container .fx2 .item {
    margin: 0 !important;
    padding: 0;
    cursor: pointer;
    overflow: hidden;
    width: 100%;
    height: 100%;
}

.gallery-container .fx2 .item img {
    padding: 0 !important;
    display: block;
    max-width: 100%;
    height: auto;
    width: 100%;
    object-fit: cover;
    aspect-ratio: 1 / 1; /* Ensure consistent sizing */
}

.gallery-container .fx2 .image-link:hover .item img,
.gallery-container .fx2 .image-link:focus .item img {
    opacity: 0.9;
    transform: scale(0.95);
}

.gallery-container .fx2 h4,
.gallery-container .fx2 p {
    transition: all var(--gallery-transition-duration) ease;
}

.gallery-container .fx2 .image-link .item h4 {
    font-family: "Raleway", sans-serif;
    font-size: 16px;
    color: var(--gallery-primary-color);
    text-transform: uppercase;
    letter-spacing: 2px;
    position: absolute;
    top: 42%;
    left: 0;
    right: 0;
    margin: 0 auto;
    text-align: center;
    filter: blur(5px);
    opacity: 0;
    pointer-events: none;
}

.gallery-container .fx2 .image-link:hover .item h4,
.gallery-container .fx2 .image-link:focus .item h4 {
    filter: blur(0px);
    opacity: 1;
}

.gallery-container .fx2 .image-link .item p {
    font-family: "Raleway", sans-serif;
    font-size: 8px;
    color: var(--gallery-primary-color);
    text-transform: uppercase;
    letter-spacing: 2px;
    position: absolute;
    top: 53%;
    left: 0;
    right: 0;
    margin: 0 auto;
    text-align: center;
    opacity: 0;
    pointer-events: none;
}

.gallery-container .fx2 .image-link:hover .item p,
.gallery-container .fx2 .image-link:focus .item p {
    opacity: 1;
}

/* Modal Styles - Made larger for readability */
.gallery-container .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: var(--gallery-secondary-color);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    z-index: 10000;
    pointer-events: none;
    padding: 10px;
    box-sizing: border-box;
}

.gallery-container .modal:target {
    opacity: 1;
    visibility: visible;
    pointer-events: auto;
}

.gallery-container .modal-close {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    cursor: pointer;
    z-index: 1;
}

.gallery-container .modal-content {
    position: relative;
    max-width: 95% !important;
    max-height: 95% !important;
    text-align: center;
    transform: scale(0.8);
    transition: transform 0.3s ease;
    z-index: 2;
}

.gallery-container .modal:target .modal-content {
    transform: scale(1);
}

.gallery-container .modal-image {
    max-width: 100% !important;
    max-height: 85vh !important;
    height: auto;
    display: block;
    margin: 0 auto;
}

.gallery-container .close-button {
    height: 50px;
    width: 50px;
    position: fixed;
    top: 20px !important;
    right: 20px !important;
    box-sizing: border-box;
    line-height: 50px;
    display: inline-block;
    cursor: pointer;
    background: rgba(0, 0, 0, 0.7);
    border-radius: 50%;
    transition: background 0.3s ease;
    z-index: 3;
}

.gallery-container .close-button:before, 
.gallery-container .close-button:after {
    transform: rotate(-45deg);
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    margin-top: -2px;
    margin-left: -15px;
    display: block;
    height: 4px;
    width: 30px;
    background-color: #fff;
    transition: all 0.2s ease-out;
    border-radius: 2px;
}

.gallery-container .close-button:after {
    transform: rotate(45deg);
}

.gallery-container .close-button:hover {
    background: rgba(0, 0, 0, 0.9);
}

.gallery-container .close-button:hover:before, 
.gallery-container .close-button:hover:after {
    transform: rotate(0deg);
}

.gallery-container #close {
    display: none;
}

/* Carousel Styles */

#isolated-carousel {
    all: initial;
    display: block;
    max-width: 900px;
    margin: 20px auto;
    padding: 20px;
    position: relative;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

#isolated-carousel .carousel-slides {
    all: initial;
    display: block;
    position: relative;
    height: 500px;
    overflow: hidden;
    border-radius: 80px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    box-sizing: border-box;
}

#isolated-carousel .carousel-slide {
    all: initial;
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: black;
    box-sizing: border-box;
}

#isolated-carousel .carousel-slide.active {
    opacity: 1;
}

#isolated-carousel .carousel-slide img {
    all: initial;
    display: block;
    max-width: 100%;
    max-height: 100%;
    width: auto;
    height: auto;
    object-fit: contain;
    box-sizing: border-box;
}

#isolated-carousel .carousel-arrow {
    all: initial;
    display: block;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0,0,0,0.5);
    color: white;
    border: none;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    font-size: 24px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.3s;
    z-index: 10;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

#isolated-carousel .carousel-arrow:hover {
    background-color: rgba(0, 0, 0, 0.8);
}

#isolated-carousel .carousel-arrow.prev {
    left: 15px;
}

#isolated-carousel .carousel-arrow.next {
    right: 15px;
}

#isolated-carousel .carousel-dots {
    all: initial;
    display: flex;
    justify-content: center;
    margin-top: 20px;
    gap: 10px;
    box-sizing: border-box;
}

#isolated-carousel .carousel-dot {
    all: initial;
    display: block;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: #ccc;
    cursor: pointer;
    transition: background-color 0.3s;
    box-sizing: border-box;
}

#isolated-carousel .carousel-dot.active {
    background-color: #333;
}

/* Mobile Responsiveness */
@media (max-width: 768px) {
    
    #isolated-carousel .carousel-slides {
        height: 350px;
    }
    
    #isolated-carousel .carousel-arrow {
        width: 40px;
        height: 40px;
        font-size: 20px;
    }
}

@media (max-width: 480px) {

    #isolated-carousel .carousel-slides {
        height: 250px;
    }
    
    #isolated-carousel .carousel-arrow {
        width: 35px;
        height: 35px;
        font-size: 18px;
    }
    
    #isolated-carousel .carousel-dot {
        width: 12px;
        height: 12px;
    }
}


/* Mobile Responsiveness with horizontal gallery fix */
@media (max-width: 768px) {
    .anim-title-container {
        bottom: 15px;
        left: 15px;
    }
    
    .anim-title-line {
        margin-bottom: 3px;
    }
    
    /* Keep horizontal layout on tablet but adjust spacing */
    
    .gallery-container .close-button {
        right: 10px !important;
        top: -60px !important;
    }
    
    .gallery-container .modal-content {
        max-width: 98% !important;
        max-height: 98% !important;
    }
}

@media (max-width: 480px) {
    .anim-title-container {
        bottom: 10px;
        left: 10px;
        width: 80%;
    }
    
</style>


<!-- Gallery Section -->
<div class="gallery-container">
    <div class="container">
        <div class="fx2">
            <!-- Image 1 -->
            <a href="#image1" class="image-link">
                <div class="item col4">
                    <img class="transition img-responsive" src="{{site.baseurl}}/assets/img/Chicago%20Wrigley%20II.jpg" alt="Pearl Jam Dark Matter Tour at Chicago Wrigley - Nebula Dark">
                </div>
            </a>
            
            <!-- Image 2 -->
            <a href="#image2" class="image-link">
                <div class="item col4">
                    <img class="transition img-responsive" src="{{site.baseurl}}/assets/img/Climate-Pledge-Rehearsals.jpg" alt="Pearl Jam Dark Matter Tour at Climate Pledge Rehearsals - Crown of Light part 1">
                </div>
            </a>
            
            <!-- Image 3 -->
            <a href="#image3" class="image-link">
                <div class="item col4">
                    <img class="transition img-responsive" src="{{site.baseurl}}/assets/img/ClimatePledgeRehearsals3.jpg" alt="Pearl Jam Dark Matter Tour at Climate Pledge Rehearsals - Gold Ripples">
                </div>
            </a>
        </div>

        <!-- Gallery Modals -->
        <div class="modal" id="image1">
            <a href="#" class="modal-close"></a>
            <div class="modal-content">
                <img src="{{site.baseurl}}/assets/img/Climate-Pledge-Rehearsals.jpg" class="modal-image" alt="Modal image 1">
                <a href="#" class="close-button"></a>
            </div>
        </div>

        <div class="modal" id="image2">
            <a href="#" class="modal-close"></a>
            <div class="modal-content">
                <img src="{{site.baseurl}}/assets/img/Climate-Pledge-Rehearsals.jpg" class="modal-image" alt="Modal image 2">
                <a href="#" class="close-button"></a>
            </div>
        </div>

        <div class="modal" id="image3">
            <a href="#" class="modal-close"></a>
            <div class="modal-content">
                <img src="{{site.baseurl}}/assets/img/ClimatePledgeRehearsals3.jpg" class="modal-image" alt="Modal image 3">
                <a href="#" class="close-button"></a>
            </div>
        </div>

        <div id="close"></div>
    </div>
</div>

<!-- Photo credit -->
<p style="font-size: 0.5rem; color: grey; text-align: right; margin-top: 5px; white-space: nowrap;">
photos + BTS footage by Rob Sheridan Productions

<!-- Content Sections -->
<p>In the winter of 2024, we had the exciting opportunity to collaborate on visuals for Pearl Jam's Dark Matter World Tour. We joined an amazing creative team led by Creative Director Rob Sheridan and Producer Stephanie Sheridan.</p>

<p>The concept for the project was to create something cosmic and awe inspiring, yet human. To bring this vision to life we developed <a title="View on Instagram" href="https://www.instagram.com/reel/DAJYEZZPrTB/?utm_source=ig_web_copy_link&amp;igsh=NTc4MTIwNjQ2YQ==" target="_blank" style="color:#1316ce;">innovative techniques</a> including a custom process that allowed us to paint with light&mdash;typically only possible within the realm of still photography&mdash;to craft a vast organic cosmic structure for the opening track of the album, &ldquo;Scared of Fear.&rdquo;</p>

<!-- More Content -->
<br>
<center>
<p>Take a glimpse of our process below:</p>
<br>
<blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DAJYEZZPrTB/?utm_source=ig_embed&amp;utm_campaign=loading" data-instgrm-version="14" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:540px; min-width:326px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:16px;"> <a href="https://www.instagram.com/reel/DAJYEZZPrTB/?utm_source=ig_embed&amp;utm_campaign=loading" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%;" target="_blank"> <div style=" display: flex; flex-direction: row; align-items: center;"> <div style="background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 40px; margin-right: 14px; width: 40px;"></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 100px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 60px;"></div></div></div><div style="padding: 19% 0;"></div> <div style="display:block; height:50px; margin:0 auto 12px; width:50px;"><svg width="50px" height="50px" viewBox="0 0 60 60" version="1.1" xmlns="https://www.w3.org/2000/svg" xmlns:xlink="https://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-511.000000, -20.000000)" fill="#000000"><g><path d="M556.869,30.41 C554.814,30.41 553.148,32.076 553.148,34.131 C553.148,36.186 554.814,37.852 556.869,37.852 C558.924,37.852 560.59,36.186 560.59,34.131 C560.59,32.076 558.924,30.41 556.869,30.41 M541,60.657 C535.114,60.657 530.342,55.887 530.342,50 C530.342,44.114 535.114,39.342 541,39.342 C546.887,39.342 551.658,44.114 551.658,50 C551.658,55.887 546.887,60.657 541,60.657 M541,33.886 C532.1,33.886 524.886,41.1 524.886,50 C524.886,58.899 532.1,66.113 541,66.113 C549.9,66.113 557.115,58.899 557.115,50 C557.115,41.1 549.9,33.886 541,33.886 M565.378,62.101 C565.244,65.022 564.756,66.606 564.346,67.663 C563.803,69.06 563.154,70.057 562.106,71.106 C561.058,72.155 560.06,72.803 558.662,73.347 C557.607,73.757 556.021,74.244 553.102,74.378 C549.944,74.521 548.997,74.552 541,74.552 C533.003,74.552 532.056,74.521 528.898,74.378 C525.979,74.244 524.393,73.757 523.338,73.347 C521.94,72.803 520.942,72.155 519.894,71.106 C518.846,70.057 518.197,69.06 517.654,67.663 C517.244,66.606 516.755,65.022 516.623,62.101 C516.479,58.943 516.448,57.996 516.448,50 C516.448,42.003 516.479,41.056 516.623,37.899 C516.755,34.978 517.244,33.391 517.654,32.338 C518.197,30.938 518.846,29.942 519.894,28.894 C520.942,27.846 521.94,27.196 523.338,26.654 C524.393,26.244 525.979,25.756 528.898,25.623 C532.057,25.479 533.004,25.448 541,25.448 C548.997,25.448 549.943,25.479 553.102,25.623 C556.021,25.756 557.607,26.244 558.662,26.654 C560.06,27.196 561.058,27.846 562.106,28.894 C563.154,29.942 563.803,30.938 564.346,32.338 C564.756,33.391 565.244,34.978 565.378,37.899 C565.522,41.056 565.552,42.003 565.552,50 C565.552,57.996 565.522,58.943 565.378,62.101 M570.82,37.631 C570.674,34.438 570.167,32.258 569.425,30.349 C568.659,28.377 567.633,26.702 565.965,25.035 C564.297,23.368 562.623,22.342 560.652,21.575 C558.743,20.834 556.562,20.326 553.369,20.18 C550.169,20.033 549.148,20 541,20 C532.853,20 531.831,20.033 528.631,20.18 C525.438,20.326 523.257,20.834 521.349,21.575 C519.376,22.342 517.703,23.368 516.035,25.035 C514.368,26.702 513.342,28.377 512.574,30.349 C511.834,32.258 511.326,34.438 511.181,37.631 C511.035,40.831 511,41.851 511,50 C511,58.147 511.035,59.17 511.181,62.369 C511.326,65.562 511.834,67.743 512.574,69.651 C513.342,71.625 514.368,73.296 516.035,74.965 C517.703,76.634 519.376,77.658 521.349,78.425 C523.257,79.167 525.438,79.673 528.631,79.82 C531.831,79.965 532.853,80.001 541,80.001 C549.148,80.001 550.169,79.965 553.369,79.82 C556.562,79.673 558.743,79.167 560.652,78.425 C562.623,77.658 564.297,76.634 565.965,74.965 C567.633,73.296 568.659,71.625 569.425,69.651 C570.167,67.743 570.674,65.562 570.82,62.369 C570.966,59.17 571,58.147 571,50 C571,41.851 570.966,40.831 570.82,37.631"></path></g></g></g></svg></div><div style="padding-top: 8px;"> <div style=" color:#3897f0; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:550; line-height:18px;">View this post on Instagram</div></div><div style="padding: 12.5% 0;"></div> <div style="display: flex; flex-direction: row; margin-bottom: 14px; align-items: center;"><div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(0px) translateY(7px);"></div> <div style="background-color: #F4F4F4; height: 12.5px; transform: rotate(-45deg) translateX(3px) translateY(1px); width: 12.5px; flex-grow: 0; margin-right: 14px; margin-left: 2px;"></div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(9px) translateY(-18px);"></div></div><div style="margin-left: 8px;"> <div style=" background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 20px; width: 20px;"></div> <div style=" width: 0; height: 0; border-top: 2px solid transparent; border-left: 6px solid #f4f4f4; border-bottom: 2px solid transparent; transform: translateX(16px) translateY(-4px) rotate(30deg)"></div></div><div style="margin-left: auto;"> <div style=" width: 0px; border-top: 8px solid #F4F4F4; border-right: 8px solid transparent; transform: translateY(16px);"></div> <div style=" background-color: #F4F4F4; flex-grow: 0; height: 12px; width: 16px; transform: translateY(-4px);"></div> <div style=" width: 0; height: 0; border-top: 8px solid #F4F4F4; border-left: 8px solid transparent; transform: translateY(-4px) translateX(8px);"></div></div></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center; margin-bottom: 24px;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 224px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 144px;"></div></div></a><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/reel/DAJYEZZPrTB/?utm_source=ig_embed&amp;utm_campaign=loading" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">A post shared by Rob Sheridan (@rob_sheridan)</a></p></div></blockquote>
<script async src="//www.instagram.com/embed.js"></script><script async src="//www.instagram.com/embed.js"></script>
</center>
<br>
<p>Rob envisioned a look that was analog, organic and human rather than the typical sharp aesthetics of concert LED screens. This led us to create a soft, glowing appearance that reflected the feel and texture of film.</p>
<p>We combined over 200 hours of <a title="View on Instagram" href="https://www.instagram.com/reel/DFOH2rZzTtF/?utm_source=ig_web_copy_link&amp;amp;igsh=NTc4MTIwNjQ2YQ==" target="_blank"  style="color:#1316ce;">1000 FPS super slow-motion</a> macro footage, real NASA visuals, and archival material to create a captivating experience projected onto a 155-foot screen.</p>
<br>
<center>
<blockquote class="instagram-media" data-instgrm-permalink="https://www.instagram.com/reel/DFOH2rZzTtF/?utm_source=ig_embed&amp;utm_campaign=loading" data-instgrm-version="14" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:540px; min-width:326px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:16px;"> <a href="https://www.instagram.com/reel/DFOH2rZzTtF/?utm_source=ig_embed&amp;utm_campaign=loading" style=" background:#FFFFFF; line-height:0; padding:0 0; text-align:center; text-decoration:none; width:100%;" target="_blank"> <div style=" display: flex; flex-direction: row; align-items: center;"> <div style="background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 40px; margin-right: 14px; width: 40px;"></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 100px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 60px;"></div></div></div><div style="padding: 19% 0;"></div> <div style="display:block; height:50px; margin:0 auto 12px; width:50px;"><svg width="50px" height="50px" viewBox="0 0 60 60" version="1.1" xmlns="https://www.w3.org/2000/svg" xmlns:xlink="https://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-511.000000, -20.000000)" fill="#000000"><g><path d="M556.869,30.41 C554.814,30.41 553.148,32.076 553.148,34.131 C553.148,36.186 554.814,37.852 556.869,37.852 C558.924,37.852 560.59,36.186 560.59,34.131 C560.59,32.076 558.924,30.41 556.869,30.41 M541,60.657 C535.114,60.657 530.342,55.887 530.342,50 C530.342,44.114 535.114,39.342 541,39.342 C546.887,39.342 551.658,44.114 551.658,50 C551.658,55.887 546.887,60.657 541,60.657 M541,33.886 C532.1,33.886 524.886,41.1 524.886,50 C524.886,58.899 532.1,66.113 541,66.113 C549.9,66.113 557.115,58.899 557.115,50 C557.115,41.1 549.9,33.886 541,33.886 M565.378,62.101 C565.244,65.022 564.756,66.606 564.346,67.663 C563.803,69.06 563.154,70.057 562.106,71.106 C561.058,72.155 560.06,72.803 558.662,73.347 C557.607,73.757 556.021,74.244 553.102,74.378 C549.944,74.521 548.997,74.552 541,74.552 C533.003,74.552 532.056,74.521 528.898,74.378 C525.979,74.244 524.393,73.757 523.338,73.347 C521.94,72.803 520.942,72.155 519.894,71.106 C518.846,70.057 518.197,69.06 517.654,67.663 C517.244,66.606 516.755,65.022 516.623,62.101 C516.479,58.943 516.448,57.996 516.448,50 C516.448,42.003 516.479,41.056 516.623,37.899 C516.755,34.978 517.244,33.391 517.654,32.338 C518.197,30.938 518.846,29.942 519.894,28.894 C520.942,27.846 521.94,27.196 523.338,26.654 C524.393,26.244 525.979,25.756 528.898,25.623 C532.057,25.479 533.004,25.448 541,25.448 C548.997,25.448 549.943,25.479 553.102,25.623 C556.021,25.756 557.607,26.244 558.662,26.654 C560.06,27.196 561.058,27.846 562.106,28.894 C563.154,29.942 563.803,30.938 564.346,32.338 C564.756,33.391 565.244,34.978 565.378,37.899 C565.522,41.056 565.552,42.003 565.552,50 C565.552,57.996 565.522,58.943 565.378,62.101 M570.82,37.631 C570.674,34.438 570.167,32.258 569.425,30.349 C568.659,28.377 567.633,26.702 565.965,25.035 C564.297,23.368 562.623,22.342 560.652,21.575 C558.743,20.834 556.562,20.326 553.369,20.18 C550.169,20.033 549.148,20 541,20 C532.853,20 531.831,20.033 528.631,20.18 C525.438,20.326 523.257,20.834 521.349,21.575 C519.376,22.342 517.703,23.368 516.035,25.035 C514.368,26.702 513.342,28.377 512.574,30.349 C511.834,32.258 511.326,34.438 511.181,37.631 C511.035,40.831 511,41.851 511,50 C511,58.147 511.035,59.17 511.181,62.369 C511.326,65.562 511.834,67.743 512.574,69.651 C513.342,71.625 514.368,73.296 516.035,74.965 C517.703,76.634 519.376,77.658 521.349,78.425 C523.257,79.167 525.438,79.673 528.631,79.82 C531.831,79.965 532.853,80.001 541,80.001 C549.148,80.001 550.169,79.965 553.369,79.82 C556.562,79.673 558.743,79.167 560.652,78.425 C562.623,77.658 564.297,76.634 565.965,74.965 C567.633,73.296 568.659,71.625 569.425,69.651 C570.167,67.743 570.674,65.562 570.82,62.369 C570.966,59.17 571,58.147 571,50 C571,41.851 570.966,40.831 570.82,37.631"></path></g></g></g></svg></div><div style="padding-top: 8px;"> <div style=" color:#3897f0; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:550; line-height:18px;">View this post on Instagram</div></div><div style="padding: 12.5% 0;"></div> <div style="display: flex; flex-direction: row; margin-bottom: 14px; align-items: center;"><div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(0px) translateY(7px);"></div> <div style="background-color: #F4F4F4; height: 12.5px; transform: rotate(-45deg) translateX(3px) translateY(1px); width: 12.5px; flex-grow: 0; margin-right: 14px; margin-left: 2px;"></div> <div style="background-color: #F4F4F4; border-radius: 50%; height: 12.5px; width: 12.5px; transform: translateX(9px) translateY(-18px);"></div></div><div style="margin-left: 8px;"> <div style=" background-color: #F4F4F4; border-radius: 50%; flex-grow: 0; height: 20px; width: 20px;"></div> <div style=" width: 0; height: 0; border-top: 2px solid transparent; border-left: 6px solid #f4f4f4; border-bottom: 2px solid transparent; transform: translateX(16px) translateY(-4px) rotate(30deg)"></div></div><div style="margin-left: auto;"> <div style=" width: 0px; border-top: 8px solid #F4F4F4; border-right: 8px solid transparent; transform: translateY(16px);"></div> <div style=" background-color: #F4F4F4; flex-grow: 0; height: 12px; width: 16px; transform: translateY(-4px);"></div> <div style=" width: 0; height: 0; border-top: 8px solid #F4F4F4; border-left: 8px solid transparent; transform: translateY(-4px) translateX(8px);"></div></div></div> <div style="display: flex; flex-direction: column; flex-grow: 1; justify-content: center; margin-bottom: 24px;"> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; margin-bottom: 6px; width: 224px;"></div> <div style=" background-color: #F4F4F4; border-radius: 4px; flex-grow: 0; height: 14px; width: 144px;"></div></div></a><p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;"><a href="https://www.instagram.com/reel/DFOH2rZzTtF/?utm_source=ig_embed&amp;utm_campaign=loading" style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none;" target="_blank">A post shared by Rob Sheridan (@rob_sheridan)</a></p></div></blockquote>
<script async src="//www.instagram.com/embed.js"></script>
</center>
<br>
<!-- Carousel -->
<div id="isolated-carousel">
    <div class="carousel-slides">
        <!-- Slide 1 -->
        <div class="carousel-slide active">
            <img src="{{site.baseurl}}/assets/img/Vancouver-BC-II.jpg" alt="Pearl Jam Dark Matter Tour at Vancouver BC - Crown of Light p2">
        </div>
        
        <!-- Slide 2 -->
        <div class="carousel-slide">
            <img src="{{site.baseurl}}/assets/img/ClimatePledgeRehearsals2 .jpg" alt="Pearl Jam Dark Matter Tour at Climate Pledge Rehearsals - The Sun p1">
        </div>
        
        <!-- Slide 3 -->
        <div class="carousel-slide">
            <img src="{{site.baseurl}}/assets/img/Vancouver BC II  (1).jpg" alt="Pearl Jam Dark Matter Tour at Vancouver BC - The Sun p2">
        </div>
        
        <!-- Slide 4 -->
        <div class="carousel-slide">
            <img src="{{site.baseurl}}/assets/img/Vancouver BC II.jpg" alt="Pearl Jam Dark Matter Tour at Vancouver BC - React Respond">
        </div>

        <!-- Slide 5 -->
        <div class="carousel-slide">
            <img src="{{site.baseurl}}/assets/img/Chicago Wrigley I (2).jpg" alt="Pearl Jam Dark Matter Tour at Chicago Wrigley - Crown of Light Wide">
        </div>

        <!-- Slide 6 -->
        <div class="carousel-slide">
            <img src="{{site.baseurl}}/assets/img/Chicago Wrigley I.jpg" alt="Pearl Jam Dark Matter Tour at Chicago Wrigley - Purple Ripples">
        </div>
        
        <!-- Navigation Arrows -->
        <button class="carousel-arrow prev">&#10094;</button>
        <button class="carousel-arrow next">&#10095;</button>
    </div>
    
    <!-- Dots Indicator -->
    <div class="carousel-dots">
        <span class="carousel-dot active" data-index="0"></span>
        <span class="carousel-dot" data-index="1"></span>
        <span class="carousel-dot" data-index="2"></span>
        <span class="carousel-dot" data-index="3"></span>
        <span class="carousel-dot" data-index="4"></span>
        <span class="carousel-dot" data-index="5"></span>
    </div>
</div>

<br>
<p>Directed by @rob_sheridan<br />Produced by @stephanie_sheridan_<br />Post production, animation, and compositing by @joybirdstudios<br />Camera Operator: @donovonmedia<br />PA: @ilanarahaman<br />Filmed at Rob Sheridan Productions, Tacoma, WA.<br />Based on the Dark Matter album art light painting photography by @fdu4<br /><br />Tour production design by @nimblist<br />Tour lighting director: @kkpearl66<br />Tour video programming: @mcdonaldg
</p>
<a href="https://pearljam.com/news/dark-matter-world-tour-2024" target="_blank">


  Pearl Jam Dark Matter World Tour 2024.


</a>


<p>


<script>
document.addEventListener('DOMContentLoaded', function() {

    initCarousel('isolated-carousel');
    
    function initCarousel(carouselId) {
        const carousel = document.getElementById(carouselId);
        
        if (!carousel) return;
        
        const slides = carousel.querySelectorAll('.carousel-slide');
        const dots = carousel.querySelectorAll('.carousel-dot');
        const prevBtn = carousel.querySelector('.carousel-arrow.prev');
        const nextBtn = carousel.querySelector('.carousel-arrow.next');
        
        let currentSlide = 0;
        const totalSlides = slides.length;
        
        function showSlide(index) {
            slides.forEach(slide => {
                slide.classList.remove('active');
            });
            
            dots.forEach(dot => {
                dot.classList.remove('active');
            });
            
            slides[index].classList.add('active');
            dots[index].classList.add('active');
            
            currentSlide = index;
        }
        
        function nextSlide() {
            let nextIndex = currentSlide + 1;
            if (nextIndex >= totalSlides) {
                nextIndex = 0;
            }
            showSlide(nextIndex);
        }
        
        function prevSlide() {
            let prevIndex = currentSlide - 1;
            if (prevIndex < 0) {
                prevIndex = totalSlides - 1;
            }
            showSlide(prevIndex);
        }
        
        if (nextBtn) nextBtn.addEventListener('click', nextSlide);
        if (prevBtn) prevBtn.addEventListener('click', prevSlide);
        
        dots.forEach(dot => {
            dot.addEventListener('click', function() {
                const slideIndex = parseInt(this.getAttribute('data-index'));
                showSlide(slideIndex);
            });
        });
        
        // Auto-advance slides
        let slideInterval = setInterval(nextSlide, 5000);
        
        const carouselSlides = carousel.querySelector('.carousel-slides');
        if (carouselSlides) {
            carouselSlides.addEventListener('mouseenter', () => {
                clearInterval(slideInterval);
            });
            
            carouselSlides.addEventListener('mouseleave', () => {
                slideInterval = setInterval(nextSlide, 5000);
            });
            
            // Touch swipe support
            let startX = 0;
            let endX = 0;
            
            carouselSlides.addEventListener('touchstart', (e) => {
                startX = e.touches[0].clientX;
            });
            
            carouselSlides.addEventListener('touchend', (e) => {
                endX = e.changedTouches[0].clientX;
                handleSwipe();
            });
            
            function handleSwipe() {
                const swipeThreshold = 50;
                
                if (startX - endX > swipeThreshold) {
                    nextSlide();
                } else if (endX - startX > swipeThreshold) {
                    prevSlide();
                }
            }
        }
    }
});
</script>
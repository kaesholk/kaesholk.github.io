---
layout: page
title: audacious corruptions
description: corrupting image files using audio editing
img: /assets/img/corruptions2/nib_echo.jpg
importance: 3
category: 2022
---

Ever since I discovered you could import raw data into the audio editing program Audacity, I wondered if you could run a file through audio effects and re-export it as a viewable image file. After some googling, I landed on this process:

1. convert your image to .tif
2. open Audacity and go to file -> import -> raw data
3. select the image and set encoding to "U-Law" and byte order to little-endian
4. apply effects to the audio newly created track 
   (do not change the beginning/end of the audio or change the overall length because the file will be unopenable)
5. go to export -> export audio
6. save as type "other uncompressed files"
7. set header to "RAW (header-less)" and encoding to "U-Law"
6. save as a new, artistically corrupted .tif file
    

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columns.jpg" title="uncorrupted image" class="img-fluid z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columnsecho.jpg" title="image with echo effect" class="img-fluid z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columns_micro_shift2.jpg" title="pitch shifted image" class="img-fluid z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columns_eq_4.jpg" title="image with eq" class="img-fluid z-depth-1" %}
    </div>
</div>
<div class="caption">
    From left to right: the original image, the same image with an echo effect, the image pitch shifted up by a very tiny amount, and the image with an EQ applied.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columns_wah_reallyslow.jpg" title="image with wah-wah effect" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions/columnsreverse.jpg" title="image with reverse effect" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: the image with a wah-wah effect. Right: the image with the middle section reversed. Interestingly, reversing the audio inverts the colors while also flipping the image.
</div>


After messing around with various effects on this example image, I tried corrupting some of my own photos.

<div class="row justify-content-sm-center">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions2/windows_echo.jpg" title="image of the side of a building with an echo effect" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions2/nib_echo.jpg" title="image of a large building with an echo effect" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/corruptions2/grate_echo.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Changing the parameters of the echo effect can change the craziness of the image.
</div>

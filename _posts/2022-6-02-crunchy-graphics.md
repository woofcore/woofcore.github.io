---
layout: post
title: 'Giving graphics CRUNCH.'
hidden: false
---

How to make graphics look "Crunchy".

<!--more-->
What do I mean by "Crunchy"?

I define “Crunch” as being vaguely reminiscent of old PC-98 graphics. That is, low colour count, high dithering, and massive contrast + saturation. Here’s an example.

Take this random image: (credit: textures.com)

![TexturesCom_LandscapesCityNight0015_2_M.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2a8ee074-db66-41c5-ab90-26267b4494fc/TexturesCom_LandscapesCityNight0015_2_M.jpg)

I use [Paint.NET](http://Paint.NET) because of its aforementioned lightweightness and simplicity. Plus, its free! 

I first resize the image using Nearest Neighbour interpolation.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/389d0df7-bf15-4d8d-9fdb-fd47d5c1bed6/Untitled.png)

I pick a random standard size, usually 512 pixels for large textures or whatever multiple of 64 is closest to the initial size. Nearest neighbour crunches it down in a way that makes it look pixellated. Like so:

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/95698305-cd6d-4664-af2b-aa1ed18307a4/Untitled.png)

Then, I run Quantize over it, with the colours set low enough that banding & dithering starts to appear, but without looking *too* weird.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13d6b2f6-9fff-43f4-b263-9cc9d31c92dd/Untitled.png)

This is different for each image depending on the amount of colours present, but I find that a good value is 64 for larger images and 24 for lower. The dithering is also set as high as it will go. The transparency threshold is good for images with alpha, creating hard edges depending on the threshold. Here’s what that looks like:

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37530389-0177-47c9-b600-6021c9229673/Untitled.png)

We’re already getting close to the PC-98 effect, but I want to go a little further. This image is too *balanced*, too *good-looking*. Lets make it truly crunchy. A good way of doing this is using Posterize, which further crunches the colours down.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e8758441-c69f-4ab2-bdce-a2314d500b4f/Untitled.png)

The values here are basically random. The only rule is that it looks good in the preview. Pretty much, go as low as possible before it starts looking “too weird”. Here’s what that looks like:

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bc3500ec-30dc-4af1-ad4b-95ccbc32153c/Untitled.png)

Now, Brightness & Contrast, which are self-explanatory. This is totally up to what I think looks good at the time, but the value changes are usually pretty subtle. I also tweak the Hue & Saturation to make the scene look slightly alien, the identifiable “texture” of the original image but with a subtle, weird shift. Here’s the final product:

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9c9532e-e433-428c-95a6-ef09feab24ec/Untitled.png)

I think it looks pretty cool!
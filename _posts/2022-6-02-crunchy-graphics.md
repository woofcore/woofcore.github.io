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

![original image](/images/crunch_original.jpg)

I use Paint.NET because of its aforementioned lightweightness and simplicity. Plus, its free! 

I first resize the image using Nearest Neighbour interpolation.

![resize dialogue](/images/crunch_resize.png)

I pick a random standard size, usually 512 pixels for large textures or whatever multiple of 64 is closest to the initial size. Nearest neighbour crunches it down in a way that makes it look pixellated. Like so:

![resized image](/images/crunch_resize_example.png)

Then, I run Quantize over it, with the colours set low enough that banding & dithering starts to appear, but without looking *too* weird.

![quantize dialogue](/images/crunch_quantize.png)

This is different for each image depending on the amount of colours present, but I find that a good value is 64 for larger images and 24 for lower. The dithering is also set as high as it will go. The transparency threshold is good for images with alpha, creating hard edges depending on the threshold. Here’s what that looks like:

![quantized image](/images/crunch_dither_example.png)

We’re already getting close to the PC-98 effect, but I want to go a little further. This image is too *balanced*, too *good-looking*. Lets make it truly crunchy. A good way of doing this is using Posterize, which further crunches the colours down.

![posterize dialogue](/images/crunch_posterize.png)

The values here are basically random. The only rule is that it looks good in the preview. Pretty much, go as low as possible before it starts looking “too weird”. Here’s what that looks like:

![posterized image](/images/crunch_posterize_example.png)

Now, Brightness & Contrast, which are self-explanatory. This is totally up to what I think looks good at the time, but the value changes are usually pretty subtle. I also tweak the Hue & Saturation to make the scene look slightly alien, the identifiable “texture” of the original image but with a subtle, weird shift. Here’s the final product:

![final image](/images/crunch_final.png)

I think it looks pretty cool!

Thanks for reading :o)
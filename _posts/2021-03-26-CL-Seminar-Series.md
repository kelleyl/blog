---
layout: post
title:  Multimodal Annotation Strategies for Images
date: 2015-05-15 21:01:00
description: 
---
I will be discussing an annotation tool and strategy for annotating images from a recipe book. The motivation for this annotation aligns with the motivations for the other recipe annotations we've discussed. We want to integrate the modalities of text and image to facilitate reasoning around the cooking task. 

First I will introduce the VIA (VGG Image Annotator) tool. This tool is from the VGG team at Oxford. This tool is writing using basic web technologies ie. HTML, CSS, and Javascript. The tool allows you to annotate images with bounding boxes or polygons then assign attributes to the regions using standard html form components. 

#A demo of the VIA tool
Now we'll take a look at some images from a recipe book in VIA.
In the first image, (pg 53) we see the first 8 steps for a `Basic No-Knead Bread` recipe.
At the bottom of the page we can see a caption describing each of the images.
To annotate the first step image, text pair, we will start by drawing a bounding box around the image for step 1 and the corresponding text for step one.
In order to link the text box to the image box, we will label each box with an id corresponding to the step number.
To complete the annotation of the step text bounding box, we will transcribe the text.
Next, within the image for step 1, we will draw bounding polygons around each prop and ingredient.
For each of the bounding polygons, if the ingredient or prop is explicit in the step, we mark it as explicit by specify the text from the step that refers to that ingredient or prop.
Now from these annotations, we can link the step to the image and its props using the step id. For each prop and ingredient, we know if it is implicit or explicit based on the whether or not there is a reference to the step. If it is an explicit ingredient or prop, we know how it is referenced in the step.

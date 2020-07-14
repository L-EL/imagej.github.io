---
autogenerated: true
title: Talk ›Image Expression Parser
breadcrumb: Talk Image Expression Parser
layout: page
author: test author
categories: 
description: test description
---

## Wish list for this plugin

We are interested into knowing how we should extend this plugin so that it suits your need. Tell us here. [JeanYvesTinevez](User:JeanYvesTinevez "wikilink")

## Additional scripts

I would like additional scripting examples. In particular... I want to be able to call it from a ImageJ Macro.

Here is an example I was able to create using javascript instead. [Jchanson](User:Jchanson "wikilink") ([talk](User_talk:Jchanson "wikilink")) 15:49, 5 November 2013 (CST)

``` javascript
// This script was created as an javascript equivalent of the Python example here:
//   http://fiji.sc/Image_Expression_Parser#Calling_the_plugin_from_elsewhere

importClass(Packages.fiji.process.Image_Expression_Parser); 
importClass(java.util.HashMap);
importPackage(Packages.mpicbg.imglib);

expression = 'A^2';

imp = IJ.getImage();

img = Packages.mpicbg.imglib.image.ImagePlusAdapter.wrap(imp);

imgMap = new java.util.HashMap();
imgMap.put('A', img);
parser = new Packages.fiji.process.Image_Expression_Parser();
parser.setImageMap(imgMap);
parser.setExpression(expression);
parser.process();
result = parser.getResult();
resultImp = Packages.mpicbg.imglib.image.display.imagej.ImageJFunctions.copyToImagePlus(result);
IJ.run(resultImp, "Enhance Contrast", "saturated=0.35");
resultImp.show();
```
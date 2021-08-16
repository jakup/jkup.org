+++ 
draft = false
date = 2021-08-16T00:00:00-04:00
title = "Hello world"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

![Hi Everybody!](hi-everybody.png)

Hi everybody!  This is my first post.
- I've recently been learning some [hugo](https://gohugo.io/), a static site generator, using the [hugo-coder theme](https://themes.gohugo.io/themes/hugo-coder/).
- I made this favicon logo using [inkscape](https://inkscape.org/) and generated the pattern with [trianglify](https://github.com/qrohlf/trianglify).

![The logo](/img/favicon.svg)

- This is how I generated the pattern using [nodejs](https://nodejs.org/).

{{< highlight javascript >}}
'use strict';
const trianglify = require('trianglify');
const fs = require('fs');

const svg = trianglify({
        width: 960,
        height: 540,
        cellSize: 15,
        variance: 0.89,
        xColors: 'YlGn',
        colorFunction: trianglify.colorFunctions.sparkle(0.2),
}).toSVG();

fs.writeFileSync('pattern.svg', svg.toString());
{{< /highlight >}}

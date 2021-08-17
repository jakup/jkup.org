+++ 
draft = false
date = 2021-08-16T00:00:00-04:00
title = "大家好"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

![大家好!](hi-everybody.png)

大家好！这是我第一次博文。不好意思我的中文不好。
- 我最近学一点[hugo](https://gohugo.io/)。
- 我用[inkscape](https://inkscape.org/)和[trianglify](https://github.com/qrohlf/trianglify)做了这个标识

![标识](/img/favicon.svg)

- 这是我用[nodejs](https://nodejs.org/)生成图案的方式。

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

fs.writeFileSync('图案.svg', svg.toString());
{{< /highlight >}}

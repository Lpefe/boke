---
title: 判断终端类型
date: 2018-04-14 09:47:13
tags:
    - js
categories:
    - 技术
##tranquilpeak添加的属性
disqusIdentifier: fdsF34ff34
keywords:
- javascript
clearReading: true
thumbnailImage: https://res.cloudinary.com/ddb5vwne6/image/upload/v1597758372/timg_fy8o3h.jpg
thumbnailImagePosition: left
autoThumbnailImage: yes
metaAlignment: center
coverImage: cover-v1.2.0.jpg
coverCaption: "A beautiful sunrise"
coverMeta: out
coverSize: partial
comments: false
meta: false
actions: false
---
处理兼容时常常需要判断终端类型

<!--excerpt-->
{% codeblock %}
var u = navigator.userAgent;
var isAndroid = u.indexOf('Android') > -1 || u.indexOf('Adr') > -1; //android终端
var isiOS = !!u.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/); //ios终端
var agent = navigator.userAgent.toLowerCase();
var isMac = /macintosh|mac os x/i.test(navigator.userAgent);
if (agent.indexOf("win32") >= 0 || agent.indexOf("wow32") >= 0) {
console.log(Windows32)
}
if (agent.indexOf("win64") >= 0 || agent.indexOf("wow64") >= 0) {
console.log(Windows63)
}
if (isMac && !u.match(/AppleWebKit.*Mobile.*/)) {
console.log(mac)
}
if (isAndroid) {
console.log(android)
}
if (isiOS && !!u.match(/AppleWebKit.*Mobile.*/)) {
console.log(ios)
}
{% endcodeblock %}
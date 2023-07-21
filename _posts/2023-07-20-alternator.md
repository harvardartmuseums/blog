---
layout: post
title:  "Hackathon 2023: Alternator"
date:   2023-07-20 14:58:52 -0400
categories: accessibility apps
---

Our hackathon project idea was to create a Chrome extension that could be used by anyone who displays a large collection of images on their site in order to collect alt and description text from relevant users. And we did it!

## Alternator

![a screenshot of an object page on the Harvard Art Museums website with a red "ALT" button above the object image](/images/2023/alternator_button.png)

Alternator gives visitors of object detail pages on our site an opportunity to provide alt and description text for objects that are missing these details. 

![a screenshot of the alternator submission for with fields for alt text, description text, and the user email address.](/images/2023/alternator_form.png)

Along with the user input, alternator sends other identifying information for the object that will help us review, approve, and eventually update the object records to improve accesibility.

The object's identifying information lives in alternator specific meta tags. The meta block also includes a link to our description guidelines and an id that is used for the form submission.

```
<!-- Alternator Meta Block -->
<meta name="alternator-id" content="320567">
<meta name="alternator-url" content="https://hvrd.art/o/320567">
<meta name="alternator-contact" content="am_moderncontemporary@harvard.edu">
<meta name="alternator-guide" content="https://s3.amazonaws.com/media.harvardartmuseums.org/assets/files/HAM_image-description-guidelines_2020_03-25_final.pdf">
<meta name="alternator-target" content="sm">
<meta name="alternator-path" content="[google sheet or sheetmonkey id]">
<meta name="alternator-container" content="image-container">
<!-- End Alternator Meta Block -->
```
## Use it!
By including the object and site specific details in a meta block, we built something that can be used by other institutions when they make their own data available to the script.

The resulting extension is not in the official Chrome extension store, but it lives on [github](https://github.com/harvardartmuseums/alternator) and is available to be run as a local Chrome extension or included in site as a javascript package.

We are deciding how we will be using Alternator on harvardartmuseums.org and who we will be asking to submit information. We'll keep you posted on any new features and implementation.
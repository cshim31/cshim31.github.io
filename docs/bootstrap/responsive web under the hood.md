---
layout: default
title: Responsive web under the hood
parent: bootstrap
nav_order: 1
---

## Purpose
I became curious about how modern webs build and maintain responsive website. I examined boostrap as it has been popular css frameworks for modern web development.

## Grid System
Bootstrap introduces its responsive and scalable view for different screen size of devices

<img src="/assets/072323/1.png" alt="Bootstrap grid system description" width="750" height="450">

Its view uses "container" and "row".

Let's examine their logic

<img src="/assets/072323/2.png" alt="Bootstrap grid system description" width="750" height="450">

Bootstrap sets breakpoint for each screen size based on types of device.
Bootstrap container only does one thing: It sets maximum width of content.

How was maximum size determined?

<img src="/assets/072323/3.png" alt="Bootstrap grid system description" width="750" height="450">



<img src="/assets/072323/4.png" alt="Bootstrap grid system description" width="750" height="450">

Bootstrap officially shows its rule of breakpoint.
Container size was set as web was probably viewed in medium screen (<1140px).
That's simple.
Key of responsiveness will probably be in "row".

<img src="/assets/072323/5.png" alt="Bootstrap grid system description" width="750" height="450">

A "row" is shown as flex box.
It sets to flex-wrap items, maintaining its width controllable while growing vertically when more items are added.

<img src="/assets/072323/6.png" alt="Bootstrap grid system description" width="750" height="450">

Web contents goes in to coulmn of row.
Bootstrap sets fixed width of column and set them to not either grow or shrink.

{: .note }
Bootstrap divides each row by 12 columns. col-md-2 means using 2 coulmn of single row, taking 1/6 portion of row.

<img src="/assets/072323/7.png" alt="Bootstrap grid system description" width="750" height="450">
<img src="/assets/072323/8.png" alt="Bootstrap grid system description" width="750" height="450">

Key was flex and ratio of width.

# Conclusion
We took a look into bootstrap to study modern web responsiveness and scalability.
They achieved it via flex layout and proportional width relative to viewport .
Understanding it will help buildnig web architecture using css and better looking website.

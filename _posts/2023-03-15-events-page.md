---
layout: post
title:  "Events page: UI and Accessibility"
date:   2023-03-15 14:58:52 -0400
categories: refresh userexperience accessibility
---

During the beta testing phase of the new site, we received feedback on both newly developed features along with elements of the site we had updated structurally but not functionally. 

One instance where we decided to add a small update was on the events page.

![View of full events listing](/images/2023/events_full_listing.png)

The calendar widget filters the events once you click on a day or advance to a new month, but a beta user pointed out that there wasn't a way to return to the full events listing using the the on page navigation available.

Without redesigning the page, the simple additon of some on screen text and a button when applicable gives the user more control. 

![April events listing](/images/2023/april_events.png)

## Text "role"

Adding a "role" to an html element can help the browser alert a user to a an item that requires attention. The dynamic text we added changes as the month changes and should be defined with one of the [live region roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles#4._live_region_roles).

```
<p class="w-full text-sm py-2 lg:py-0 lg:-mt-8 lg:mx-auto lg:px-4 lg:w-[32rem] lg:-mt-45">

  <button class="py-2 px-4 text-white bg-hamdarkgray hover:bg-black" type="button" @click="[clearMonth(), getNoOfDays()]">View all upcoming events</button>

  <span class="px-2" role="status" x-text="`(viewing events for ${MONTH_NAMES[month]})`">(viewing events for April)</span> 
  
</p>

```
The 'role' is clearly defined for the text as 'status' (see the the code snippet above). This way, when turned on, a screen reader will jump to alerting the user that one of their interactions resulted in the appearance of a new element and descriptive text.

## Role in action
Here's a video of a screen reader alerting the user to the 'status' changes as they happen:

<video width="100%" preload="auto" controls>
  <source src="/images/2023/events_calendar.mp4" type="video/mp4">
</video>

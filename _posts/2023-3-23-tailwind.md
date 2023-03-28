---
layout: post
title:  "Tailwind CSS"
date:   2023-03-23 14:58:52 -0400
categories: refresh 
---

People who like to have total control over custom components and weilding the latest CSS features as they are adopted across browsers may be a bit hesitant to use a library like Tailwind. In fact, the syntax allows several ways to add custom values if the predefined utilities fall short. Here are a few of the features that made Tailwind easy to use along with leading to general code health improvements during the site refresh.

## Utility-First

Sarah Dayan's talk [In Defense of Utility-First CSS](https://www.youtube.com/watch?v=R50q4NES6Iw&ab_channel=dotconferences) hits many of the benefits of tying your CSS to your style guide with a utility library rather than writing CSS to style your project as it evolves.

Basically, a utility-first framework like Tailwind allows you to style an html componenent by chaining many specific classes together in order to achieve a design rather than writing custom CSS for every new componenet or changing the class name and/or CSS as the component's uses evolve.

## Compiled CSS of used classes only

Often, the first use of an html component dictiates the class name. This often leads us to create duplicate CSS with a new component name when a slight variation or update is needed. We can lose sight of how the html and CSS are connected and end up with a lot of unused code. With Tailwind, the CSS is comprised of only the classes actiely being used in the html. Whether they are utility classes or custom defined classes (yes, you can add custom CSS!), the compiled file will never be bloated. 

## Clear and logical naming conventions

Tailwind utility class names describe exactly what they do. 'x' and 'y' along with numbers are used to describe utilities for padding and margin. Following are some spacing utility names and their corresponding CSS.

```
py-px	
padding-top: 1px;
padding-bottom: 1px;

py-2	
padding-top: 0.5rem; /* 8px */
padding-bottom: 0.5rem; /* 8px */

p-4	
padding: 1rem; /* 16px */

px-4	
padding-left: 1rem; /* 16px */
padding-right: 1rem; /* 16px */

```

The base pixels can be set to align with your style guide. In use, the classes help increment spacing consistently. Still, Tailwind allows using [arbitrary values](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values) with brackets that work in tandem with the class prefixes or as inline styles. Complete custom control is always a possibility in Tailwind but rarely necessary if you have a good style guide.

## Defining components with utilities

Do you find yourself repeatedly using the same utility classes for a basic layout? Tailwind accomodates grouping those with a custom class (along with the option of writing completely custom CSS) and making them globally accessible through a utility or component class. This can be particularly useful for maintaining readable code and applying different component layouts across breakpoints. For example, defininig '.card-compact' and '.card' allows you to set the breakpoint for these layouts in the html component:

```
<div class="card-compact lg:card">
  <!-- ... -->
</div>

```
Similar to Tailwind breakpoints, all of the other syntax rules apply to custom classes. For instance, adding other Tailwind utilities (or arbitrary vaules) after the custom classes allows you to override styles defined in the custom classes. The arbitrary value 'p-[24px]' below will override any padding settings defined in 'card-compact'.

```
<div class="card-compact p-[24px] lg:card">
  <!-- ... -->
</div>

```

## TL;DR

Tailwind maintians the cascading logic of CSS, keeping the mixing of utility classes and custom styles intuitive. Slight variations can be achieved by adding classes rather than writing CSS, but custom solutions are not only possible but easily integrated at many points with Tailwind.
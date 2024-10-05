---
title: "Thoughts on Hugo and Web Apps Development"
date: 2024-10-04
lastmod: 2024-10-04
draft: false
garden_tags: ["Thoughts", "Technology"]
summary: " "
status: "growing"
---
# Description

This article elaborates the author's feeling at his first attempt using Hugo as a web framework. This article compares Hugo's hands-on experience with other web frameworks, mainly Django, with which the author is more familiar.

# Author

Chris Wang, the author, is a student in the M.S. in Data Science Program at Northwestern University, Evanston. The author has about one year of full-time web application development experience and considered himself familiar with full-stack web development.

# Hugo's Hands-on Experience

## Easy to use

### Easy to Modify
If we don't consider contemporary (modulizaed) frontend frameworks such as React and Vue, modifying a project at the level of "codes", or html, css, and JavaScript, can be an extremely challenging task. The overlapping relationships between elements in native frontend frameworks can be very complex, especially when it comes to large-scale projects. After that, the next major chllenge is the loading order of elements by the frontend engine. These issues arise because the modifiers are not as familiar with the structure of the template as the template makers are.

When I was assigned, as a course project, to form a website from an existing template using Hugo, I started very early. Because I understand how time-consuming this can be. However, the time consumed in this task is surprisingly low.

Hugo's projects are very well-structured. In another word, its various modules are well divided and encapsulated. <code>layout</code>, for example, contains static files such as htmls, that are to be rendered by the frontend engine. <code>content</code>, on the other hand, includes textualized <code>.md</code> files that store contents. Levels (the organization of URLs) are defined directly by the folders structure, which from my knowledge, are normally required to be defined in another files. Such clear hierarchy of web application's files is actually a luxury, even though a sacrifice may have been made in terms of customizability.

### Easy to Deploy
Hugo is a static web page generator. While this is normally considered less-powerful, as it cannot dynamically generate webpages, this attributes make it very convenient when deploying, comparing to well-developed and dynamic web frameworks such as Flask or Django, which are required to be runned on a functional, and usually high-performant Linux server. Not to mention their tedious deployment procedure.

Connecting Hugo to GitHub Pages is quick and simple, and it is viable because of Hugo's being a static web page generator.

### Easy to Scale
Hugo utilizes Go's template syntax that allows modifying html files in a way of programming. This is not exclusive to Hugo, but Hugo's is seemingly easier to understand and more powerful. It can handle things like loops, conditionals, and partials.

And the existance of it surprises me because I used to think that this cannot be done if there is no backend server running the codes to construct. Now I understand that even though Hugo is a static site generator, it leverages Go's templating system to provide dynamic-like functionality during the build process, not during runtime. This means that while the site is static, Hugo can still introduce a lot of flexibility when it comes to generating pages.
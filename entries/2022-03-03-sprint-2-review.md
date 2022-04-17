---
layout: post
title:  "Sprint 2 Review"
date:   2022-03-03 23:27:00 -0500
categories: cit280 reflection
---

## Documentation
The team improved at delegating tasks this sprint. Each team member picked up a mostly adequate amount of work, and completed the majority individually. As a group, we brainstormed the basic entity diagram models. These were later completed by Brandon, and then I added a few updates to fix entity relationships.

The main concern the group had was Stripe. The group decided to do research on it via the documentation. We found that, while Stripe allows for products to be added, only one image per product is allowed via the dashboard, but eight can be done via its API. After asking the product owner, we found that we needed the extra image allotment provided by the API. From here, we decided that we needed to have a database with our system. A new issue was that Stripe accepts products via JSON, which meant that if we used MSSQL, we would have to work with serialization. We came to the conclusion that, due to our familiarity with MSSQL, it would likely be better to use it. The result of these discussions is that Stripe will be handling most of our business operations, including payments, invoices, and emails. The application will handle customer interactions and the CRUD functionality for products.

On an individual level, I worked on wireframes for the product landing pages and all of the case study pages, and also created the basic persistence and model classes in the application. 

My experience with wireframes is that much of the design happens at the start with the landing page. Most components and stylings are determined here. I believe that my work early on likely saved time for the designs that other group members made. The pages should be easy to implement into an application, as I put responsive design first. This can be seen with how the layout translates between the desktop and mobile versions of the landing page.

Most of the trouble came from attempting to implement the entity diagrams into the application as models. We were storing certain properties in the entity diagrams in an improper way. For example, a product is meant to represent jewelry. Each piece of jewelry can potentially have eight images. But, our product diagram had only one image identifier property. I tried to accommodate for this issue by creating a list of images instead. However, this does not actually solve the issue, as it breaks the relationship between models. This meant having to redesign the image and product entity diagrams, and then reimplement the designs into the product classes. To apply these ideas elsewhere, I also had to redesign the order and cart entities, and add in a new cart item entity. To solve this for future applications, the best solution would be to specifically review the diagram for database rules and logic for SQL operations before implementation, which I had not done. 

## Reflection
The second sprint was a direct improvement over that of the first sprint. The team is great to work with. When we reviewed the tasks that needed to be done, everyone effortlessly chose what they wanted to work on. The resulting diagrams have been mostly good. It may be beneficial to review content more, as there are errors in the diagrams. It would be interesting to have each team member do an in-depth review of another team member's work for spelling, styling, or logical errors, but it may be unnecessary for this project.

I also feel more confident in developing applications. Initially, I was uncertain about how much input I could give for the project. After realizing that much of the work is similar to previous classes, and along with some of the self-studying I've done, I've found that most of the planning concepts and interactions between project systems are easy to understand.
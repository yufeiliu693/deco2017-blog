---
title: Planning a Modular Web App Structure
date: 2026-04-26
author: Yufei Liu
summary: This blog explains how we used Week 8 modular design thinking to organise Sydney Life Aid more clearly. Instead of designing every page separately, we planned a shared layout, reusable components, partial views, and module-based teamwork. This helped us make the website structure more consistent, easier to build, and easier to maintain later.
tags:
  - Modular Design
  - Reusable Components
  - Team Collaboration
---
## Course learning gains

In the 8th week, I realized that our web application needed to adopt a modular design. Before this, we had already regarded task cards, location cards, peer experience cards and question cards as important functions. So the next step is to use the modular design approach to create shared layouts, partial views and reusable components. This will help us complete the network setup more efficiently, facilitate website maintenance and enable better teamwork within our team.

## Part 1: Layout and Wireframes
![](assets/images/3.1.png)

After clarifying the concept of modular design, we drew layout diagrams and some sectional views, separating the shared page framework from the reusable content modules. The layout diagram serves as the backbone of the entire website, such as the header and navigation bar. The partial views are reusable components that support local updates in HTML. 

We also created wireframes to see where these modules could appear on different pages. The website structure became clearer, which was beneficial for our next construction stage and also made it easier to assign tasks among team members.

## Part 2: Selection and Components
![](assets/images/3.2.png)

After planning the layout and reusable components, we further weighed the pros and cons of the modular design. A unified navigation, card style, button rules, and database connection method can make the website look more complete and reduce repetitive work during development. However, if all the modules are made too uniform, the main task routes of users may be weakened, and the data required for different content cards may also become less compatible. Therefore, our design focus is to strike a balance between "maintaining system consistency" and "retaining page function differences", so that the components can be reused without affecting the clear path for users to complete the medical consultation task.

## Part 3: Division of Labor and Implementation
![](assets/images/3.3.png)

After all the layout schemes were completed and reusable components were confirmed, we allocated the work by modules. I was responsible for the task process/preparation module, which included the home/task page, task path, preparation steps, and the cards related to the task. Yu Xi was responsible for the location/community/experience module, including the address page, community page, post detail page, location card, peer experience card, and the operation for saving the location. 

This picture clearly shows that we have completed the page structure and modular organization of the Sydney Life Aid Project. The "partials/" folder is specifically used to store reusable components. The large image below is "views/layouts/default.html.tmpl", which is the shared layout framework for the entire website. It includes the header/navigation bar, language switching, user input boxes, the main content area, and the footer. This follows the modular design concept.

## Personal Reflection

This week, my greatest achievement was discovering that modular design involves establishing a set of structural rules that all the team members can abide by, including but not limited to page layout, component naming, and CSS class names. Through practice, I realized that if these rules are not unified, each person, when completing their own page, will have inconsistent styles, data disconnections, and difficult-to-maintain fragmented websites. Modular design also helps us solve the problem of team collaboration, allowing each member to have a clearer understanding of how their part integrates into the entire system.

### Core design decisions:
We adopt a modular design to organize the website, maintaining system consistency through sharing layouts, page templates, partial views, component naming, CSS and page styles.

### Division of labor

Joint discussion and finalization. I am responsible for creating Chart 1, while Yuxi is responsible for creating Chart 2.

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
# Web app modular design

## Learning Experience

In Week 8, I understand why our web app needs modular design. I started to understand these cards in a new way. Before this, we had already identified task cards, place cards, peer experience cards, and question cards as important functions. But Week 8 made me think about them as reusable components should follow consistent structures.This helped us plan the website in a more modular and maintainable way.

## Part Two: Layout and Wireframes
![](assets/images/3.1.png)

With modular design understood in Week 8, we started planning how this idea could be used in our website. We made a layout and partial view diagram because we needed to separate the shared page frame from reusable content modules. The layout helped us define the common structure, such as header, navigation, page container, main content area, and footer. The partial views helped us identify repeated parts, such as task cards, place cards, experience cards, question cards, filters, and saved place items. We also created wireframes to see where these modules could appear on different pages. This helped our next building stage because the website structure became clearer, more consistent, and easier to divide works between team members.

## Part Three: Selection and Components
![](assets/images/3.2.png)

With the layout and reusable components planned, we also reflected on the trade-offs of modular design. We did this because modularity is not only about splitting the website into smaller parts. Each component still needs to support a real functional requirement. We mapped components such as navigation, search bar, task cards, experience cards, place cards, save buttons and release forms to user needs. Then we listed benefits and limitations. From this, we learned that reusable components can improve consistency and teamwork, but they also need clear data, routes, CSS names and shared standards.

## Part Four: Division of Labor and Implementation
![](assets/images/3.3.png)

Once all the layout plans were completed and the reusable components were confirmed, we allocated the work by module. I was responsible for the task process/preparation module, which included the home page/task page, task path, preparation steps, and the cards related to the tasks. Yuxi was responsible for the location/community/experience module, including the address page, community page, post detail page, location card, peer experience card, and the operation for saving the location.

The picture clearly shows that we have achieved the page structure and modular organization of the Sydney Life Aid project. The "partials/" folder is specifically used to store reusable widgets. The large image below is "views/layouts/default.html.tmpl", which is the shared layout skeleton for the entire website. It includes the header/navigation, language switching, main content area, and footer. This follows the modular design concept from the 8th week. First, a unified layout is constructed, and then different functional pages are combined using page templates and partial components.

## Personal Reflection

In Week 8, I think the most difficult part was understanding modular design as both a design and teamwork decision. As a beginner, I first thought modularity only meant reusing cards, but later I realised it also required shared layout, page templates, partial views, naming rules, CSS styles, routes and data fields. Our group made a trade-off: instead of designing every page separately, we divided the website into modules. This week helped me understand that web app design is not only about pages, but also about structure, collaboration and future maintenance.

### Division of labor

Joint discussion and finalization. I am responsible for creating Chart 1, while Yuxi is responsible for creating Chart 2.

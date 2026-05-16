---
title: Connecting Implementation, Deployment and Maintenance
date: 2026-05-10
author: Yufei Liu
summary: This blog article provides a detailed account of how the Sydney Life Aid Organization transformed the page design into a functional prototype. In this study, we focused on discussing aspects such as deployment limitations, API selection, security, repetitive database operations, and maintenance decisions through user operations. These factors have made this prototype more secure and stable.
tags:
  - Implementation
  - Deployment
  - Maintenance
---
## Course learning gains

In the 10th week, I realized that our web application couldn't merely focus on the page design aspect. We needed to integrate the pages, user flows, routes, controllers, SQLite database, and some views into a usable prototype. When users perform actions on the page (such as searching, posting, saving, liking, and commenting), these actions will be transformed into server requests. Then the system will read or update the data and return the page.

## Part 1: Database Reading, User Operations and System Responses
![](assets/images/5.1.png)

In this section, we used three charts to verify whether our technical decisions truly met the user requirements. We compared each user requirement with the current MVP implementation, so that we could determine which functions have been supported and which can be implemented in the future. 

Then we identified whether each major user operation had a clear system path, from clicking a button to receiving page updates. Finally, we distinguished read operations from change operations. This made our prototype logic clearer.

## Part 2: Deployment, Integration and Future Expansion
![](assets/images/5.2.png)

In this part, we started to think about deployment and future integration more clearly. We found that different project types need different deployment methods. A1/A3 blog is a static website, so GitHub Pages and GitHub Actions can publish it automatically. But Sydney Life Aid is different. It has backend routes, SQLite database, sessions and user interactions, so it would need a hosting environment that supports server-side running.

For integration, we also made a trade-off. We did not add Map API into the MVP. Instead, we used place cards and Google Maps external links first. This still helps users find GP, pharmacy and emergency care, while avoiding API key, cost and error-handling problems.

## Part 3: Safety, Maintenance and Adjustment Implementation
![](assets/images/5.3.png)

At this stage, we started to think about security and maintenance after building the main functions. The issue was not only whether save, like or comment could work, but whether they could work safely and repeatedly. So we used validation, text cleaning and parameterised queries for user input, because release forms, comments, replies and search keywords cannot be trusted directly. For repeated actions like saving a place or liking a post, we used INSERT OR IGNORE to avoid duplicate records. We also kept config.yml and database files out of GitHub through .gitignore. This made the prototype safer, cleaner and easier to maintain.

## Personal Reflection

In this blog, I learned that implementation is not only about making functions work once. User actions can repeat, so the database needs rules to protect consistency. INSERT OR IGNORE helped us avoid duplicate save-place and like records.

### Core design decisions:
1. We divided user operations into read and modify functions, ensuring that actions such as searching, posting, saving, liking, and commenting all correspond to clear system response paths. 
2. For the time being, we will not incorporate the map API into the MVP. Instead, we will use location cards and external links to Google Maps to ensure that users can find medical facilities while reducing development costs and technical risks.

### Division of labor
Joint discussion and finalization. All charts and codes are jointly created and implemented.
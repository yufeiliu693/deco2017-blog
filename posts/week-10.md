---
title: Connecting Implementation, Deployment and Maintenance
date: 2026-05-10
author: Yufei Liu
summary: This blog explains how Sydney Life Aid moved from page design into a runnable prototype. I focused on how user actions connect with routes, controllers, SQLite data, GET / POST logic, and system responses. I also reflected on deployment limits, API trade-offs, security, repeated database actions, and maintenance decisions that make the prototype safer and more stable.
tags:
  - Implementation
  - Deployment
  - Maintenance
---
## Course learning gains

In the 10th week, I realized that our web application couldn't merely focus on the page design level. We needed to integrate the pages, user flows, routes, controllers, SQLite database and some views into a usable prototype. When users operate on the page (such as searching, posting, saving, liking and commenting), it will be transformed into a server request. Then the system will read or update the data and return the page.

## Part 1: Database Reading, User Operations and System Responses
![](assets/images/5.1.png)

In this part, we used three diagrams to check whether our technical decisions really matched the user tasks. The first table helped us compare each user requirement with the current MVP implementation, so we could see which functions were already supported and which ones were only future ideas. The request flow diagram helped us test whether every main user action had a clear system path, from clicking a button to receiving a page update. The GET / POST diagram was also useful because it forced us to separate reading actions from changing actions. This made our prototype logic clearer and easier to explain.

## Part 2: Deployment, Integration and Future Expansion
![](assets/images/5.2.png)

In this part, we started to think about deployment and future integration more clearly. We found that different project types need different deployment methods. A1/A3 blog is a static website, so GitHub Pages and GitHub Actions can publish it automatically. But Sydney Life Aid is different. It has backend routes, SQLite database, sessions and user interactions, so it would need a hosting environment that supports server-side running.

For integration, we also made a trade-off. We did not add Map API into the MVP. Instead, we used place cards and Google Maps external links first. This still helps users find GP, pharmacy and emergency care, while avoiding API key, cost and error-handling problems.

## Part 3: Safety, Maintenance and Adjustment Implementation
![](assets/images/5.3.png)

At this stage, we started to think about security and maintenance after building the main functions. The issue was not only whether save, like or comment could work, but whether they could work safely and repeatedly. So we used validation, text cleaning and parameterised queries for user input, because release forms, comments, replies and search keywords cannot be trusted directly. For repeated actions like saving a place or liking a post, we used INSERT OR IGNORE to avoid duplicate records. We also kept config.yml and database files out of GitHub through .gitignore. This made the prototype safer, cleaner and easier to maintain.

## Personal Reflection

In this blog, I learned that implementation is not only about making functions work once. User actions can repeat, so the database needs rules to protect consistency. INSERT OR IGNORE helped us avoid duplicate save-place and like records. I also learned that routes, controllers, SQL queries, HTMX updates and safety checks all need to work together as one system.

### Division of labor
Joint discussion and finalization. All charts and codes are jointly created and implemented.
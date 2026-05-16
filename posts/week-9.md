---
title: Database Implementation - DDD and ERD
date: 2026-05-03
author: Yufei Liu
summary: This blog explains how we moved from wireframes and user flow into database planning. Through DDD, ERD, technical feasibility review, and SQLite/code screenshots, we clarified which data should become core entities and which should support community interaction. This helped the project become more realistic, buildable, and connected to actual user actions.
tags:
  - Database Design
  - DDD and ERD
  - SQLite
---
## Course learning gains

In the 9th week, I began to understand that database design should be based on pages and user processes, rather than directly derived from the code. It should be determined through our wireframes and flowcharts. This made me realize that the database is not just a place to store content; it should support user operations and function realization.

## Part 1: Identifying Data, Initial DDD Data Definitions and ERD
![](assets/images/4.1.png)

First, we reviewed our wireframes and user flows, and classified the data into three categories: display data (i.e., the content shown on the page), input data (i.e., the content submitted or selected by the user), and generated data (i.e., the records updated by the system).

After listing and discussing these data requirements, we classified them into nine possible data objects and clarified the core database structure through an ERD. The main entities of this platform are: tasks, task processes, location selection, and peer experiences.

## Part 2: Consultation and Iteration
![](assets/images/4.2.png)

After completing the first Data Dictionary (DDD) and Entity Relationship Diagram (ERD), we did not directly use them as the final version. Instead, we invited a student majoring in computer science to conduct a technical feasibility review of them. The feedback indicated that if each object in the previous DDD was converted into a database table, it would increase the complexity of the connection paths, models, SQL queries, and templates. However, if we only retained the core four entities, it would feel there were no connections between them.

## Part 3: Final ddd Data Definition Table and ERD Relationship Diagram
![](assets/images/4.3.png)

After conducting a technical feasibility review, we made adjustments to the structure. For the core queryable data, we retained "task", "task steps", "location" and "peer experience" as the core data, as they support the main task path. Then, we added new entities as auxiliary data ("user", "question", "saved location", "comment" and "like"). This solved the problems of the previous version, and the new entities were also able to establish good connections with the core data. This enhanced the rational operability of the website and strengthened community interaction.

## Part 4: Database Support Pages and Implementation
![](assets/images/4.4.png)

After completing DDD and ERD, we compiled screenshots of the database and code to demonstrate how the data planning supports the actual network application. We checked the SQLite tables using DB Browser. The file src/models/medical.ts is responsible for translating the data structures determined in DDD and ERD into actual database tables and query logic. The file src/controllers/medical.ts then reads the tasks, peer experiences, comments, and saving locations from the model and passes these contents to the corresponding views. Finally, the file medical/experiences.html.tmpl uses template loops to call the experience-tile local view, displaying the user experiences in the database as post cards on the community page.

## Personal Reflection

In this blog, I mainly discussed how our data design has become more practical and feasible. Through domain-driven design (DDD), entity relationship diagram (ERD), and feasibility review, I learned that database design should not start with arbitrary tables, but should originate from the content that users see, input and generate on the website. I also learned that each data object needs to support actual page functions, routes, models, controllers and templates.

### Core design decisions:
1. Starting from the wireframes and user operations, we deduced the core data that the website must store, and retained Task, TaskStep, Place and PeerExperience to support the main task paths.

2. We adjusted the database structure based on the achievable scope of the MVP, so that data, models, controllers and pages could truly be connected, rather than just providing static displays.

### Division of labor
These decisions were discussed and finalised together. All diagrams and code implementation were created collaboratively.The iteration from Figure 1 to Figure 3 referenced the user's technical feasibility review.

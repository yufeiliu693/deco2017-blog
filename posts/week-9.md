---
title: Turning Page Needs into a Database Structure
date: 2026-05-03
author: Yufei Liu
summary: This blog explains how we moved from wireframes and user flow into database planning. Through DDD, ERD, technical feasibility review, and SQLite/code screenshots, we clarified which data should become core entities and which should support community interaction. This helped the project become more realistic, buildable, and connected to actual user actions.
tags:
  - Database Design
  - DDD and ERD
  - SQLite
---
# Database Implementation - DDD and ERD

## Classroom Learning and Gains

In Week 9, I started to understand that database design should come from pages and user flow, not directly from code. From our wireframes, we identified what data the platform needs. This helped me see the database as the system should support user behaviors, can't detached from the interface just be a place to store content.

## Part Two: Identifying Data, Initial DDD Data Definitions and ERD
![](assets/images/4.1.png)

In this part, we did not start the database design directly from code. We first looked back at our wireframes and user flow, because we needed to understand what data the website actually needs to support user actions. From this process, we divided the data into three types: displayed data, input data, and generated data. Displayed data means the content shown on the page, input data means what users submit or choose, and generated data means the records updated by the system. 

With these data needs listed and discussed, we grouped them into nine possible data objects. Then we made a decision to keep Task, Task Step, Place, and Peer Experience Card as the core database objects. We did this because these four objects directly support the main medical help pathway. Finally, we used an ERD to make the relationship between these core entities clearer, so the later database structure would built from the actual user flow and page needs.

## Part Three: Consultation and Iteration
![](assets/images/4.2.png)

Once the first Data Dictionary (DDD) and Entity Relationship Diagram (ERD) were completed, we did not directly use them as the final version. We invited a student majoring in computer science to conduct a technical feasibility review on them. The feedback indicated that if each object were transformed into a database table, it would increase the connection routes, models, SQL queries, and templates, making them overly complex. Therefore, we made adjustments to the structure. We retained "task", "task step", "location", and "peer experience" as the core data because they support the main task path. Then, we added new entities ("user", "question", "saved location", "comment", and "like") which can provide a good connection with the core data. This improves the rational operability of the website and enhances community interaction.

## Part Four: Final ddd Data Definition Table and ERD Relationship Diagram
![](assets/images/4.3.png)

Following the technical feasibility review, we made adjustments and divided the data into core queryable data and supporting/simplified data. The core entities include Task, TaskStep, Place, and PeerExperience. These entities cover task selection, step guidance, location search, and experience reading. The auxiliary entities include User, Question, SavedPlace, ExperienceComment, and ExperienceLike. These entities support login, question posting, location saving, comment reply, and like, thereby enhancing the logic of the core entities.

## Part Five: Database Support Pages and Implementation
![](assets/images/4.4.png)

At this Week 9 stage, with the DDD and ERD finished, we organised the database and code screenshots to show how the data plan could support the actual web app. We checked the SQLite tables in DB Browser, then connected the data objects to TypeScript interfaces, CREATE TABLE code, SELECT / JOIN queries, controller logic, and template loops. This helped us show the full path from database to page display. It proves the prototype was moving from planned data structure into a working data-driven web app.

## Personal Reflection

In this blog, I mainly reflected on how our data design became more realistic. Through DDD, ERD and feasibility review, I learned that database design should not start from random tables. It should come from what users see, input and generate on the website. I also learned that every data object needs to support a real page function, route, model, controller and template, otherwise it will only make the MVP harder to build.

### Division of labor
Joint discussion and finalization. All charts and codes are jointly created and implemented.

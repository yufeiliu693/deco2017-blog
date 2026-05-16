---
title: From Information Pages to a Task-Oriented Web App
date: 2026-04-18
author: Yufei Liu
summary: This blog explains how our project shifted from a normal website idea into a task-oriented web app. Through user task analysis, function prioritisation, page structure planning, user flow, and wireflow, we clarified how Sydney Life Aid should guide users through actions instead of only showing information.
tags:
  - User Flow
  - Functional Requirements
  - Task-Oriented Web App
---
## Course learning gains

At the 7th week, we hope that this platform can support actual medical tasks. I will consider it as a web application. It should not only display information but also guide users through the task steps and respond to users' questions.

## Part 1: Extracting User Tasks and Defining Function Hierarchies
![](assets/images/2.1.png)

In this section, we transformed the previous research results and pain points analysis into more clear user tasks and functional requirements. First, we identified the core functions of the website: assessing the situation, selecting the corresponding Task for the problem, viewing Peer experiences, finding the target location, saving useful information, and participating in community discussions. 

After, we compare the core functions and optional features. Through the analysis of the table, we learned that task entry, task details, step-by-step paths, location cards, and companion experience cards are the core minimum viable product functions. Other ideas, such as real-time chat, map API, badges, and intelligent recommendations, can be considered as future features. This helps our initial MVP to stay focused.

## Part 2: Overall Page Structure of the Website
![](assets/images/2.2.png)

After determining the core user tasks, we began to plan the structure of the website. We planned the pages based on the user's operation path. The home page serves as the starting point of the entire system, guiding users to the main functional pages such as the community, address, posting, and settings. The community page is used for browsing and searching for peer experiences, while the post detail page further supports reading the complete content. The posting page allows users to share their medical experiences. The address page helps users quickly find GP, pharmacies, and emergency-related locations. The plan is designed to allow users to view specific locations by opening it on Google map. The settings page centrally manages personal information, saved locations, posted content, and interaction records.

## Part 3: Website Flow and Response to User Actions
![](assets/images/2.3.png)

Before building the website, we tested its logic using wire flow. We did this because merely planning the page structure does not indicate whether the user's actual operations are consistent. Wireframes help us clearly see the relationship between the screen and the operation. For example, when a user clicks on a post in the community, they will be redirected to the detail page. Through this process, we determined which pages require buttons, feedback, and clear return paths.

## Personal Reflection

I think the most challenging part lies in transforming a broad idea into a clear network application process. It involves determining what the user should do on each page and ensuring that different pages are interconnected without confusing the user. We discussed multiple versions with my team members, and we drew many messy sketches on paper to clarify the logic. Due to the excessive complexity, we did not include it in the blog. However, through repeated discussions and user process simulations, the final idea became very clear.

### Core design decisions:
1. We organized the user's core medical assistance process into a complete operational path, and based on this, determined the main page structure of the website.

2. We separated the MVP functions from the secondary functions, and prioritized retaining the task entry, peer experience, location search, location saving, and basic inquiries that can directly support the core tasks.

### Division of labor
Conducted discussions and reached a consensus. I am responsible for creating Chart 1, while Yuxi is responsible for creating Chart 2, and Chart 3 was created jointly by us.

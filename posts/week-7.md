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

In Week 7, we already wanted the platform to support a real medical task. Week 7 helped me understand this idea more clearly as a web app. It should not only show information, but also guide user actions through task steps, place cards, save buttons, questions, and system responses.

## Part 1: Extracting User Tasks and Defining Function Hierarchies
![](assets/images/2.1.png)

For this part, we turned our earlier research and pain point analysis into clearer user tasks and functional requirements, so we made Tasks & Core Functional Requirements Table. Then we needed to know which functions must be built first, so we made another table to Compare core functions and optional functions. From the table, we learned that task entry, task detail, step-by-step path, place cards, and peer experience cards are core MVP functions. Other ideas, like real-time chat, map API, badges, and smart recommendations, can be future features. This helped our later website stay focused, realistic, and easier to build.

## Part 2: Overall Page Structure of the Website
![](assets/images/2.2.png)

With the core user tasks confirmed, we started planning the website structure. We did not organise pages like a normal website. Instead, we mapped pages from the user’s action path. This helped us decide what each page should do, such as task entry, community posts, place search, publishing, and settings. It made the next design stage clearer and more focused.

## Part 3: Website Flow and Response to User Actions
![](assets/images/2.3.png)

Before building the website, we tested the logic through a user flow. We did this because page structure alone could not show whether the user’s actions were consistent. We wanted to check the whole process when a user logs in, enters the task page, filters community posts, opens a post, saves a place, asks a question, or returns to another page. Then we made the wire flow to helped us see the connection between screens and actions more clearly. From this process, we found which pages needed buttons, feedback, and clear return paths. This helped our next building stage avoid broken or confusing user journeys.

## Personal Reflection

In Week 7, we made a trade-off here. We did not include every possible feature in the MVP. Some functions, such as full medical records, complex chat, and smart recommendations, were useful but too large. So we kept the core pathway: task entry, peer experience, place search, save place, and basic questions.

I think the most difficult part was turning a broad idea into a clear web app flow. As a beginner, it was not hard to imagine pages, but it was harder to decide what the user does on each page, what the system should show next, and how different pages connect without making users confused. During this process, I and my team members discussed multiple times. I and my team members discussed several versions. The content of our discussions was not limited to how various functions should be divided onto appropriate pages, and setting appropriate buttons on each page to jump to the next page, etc. That early ideas were only messy sketches on paper, so we did not include them in the blog. But through repeated discussion and user-flow simulation, the final diagram became clearer. I found that when we explained ideas to each other, logic problems appeared quickly.

### Division of labor
Conducted discussions and reached a consensus. I am responsible for creating Chart 1, while Yuxi is responsible for creating Chart 2, and Chart 3 was created jointly by us.

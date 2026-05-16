---
title: Testing the MVP and Planning the Next Iteration
date: 2026-05-14
author: Yufei Liu
summary: This blog reflects on the Sydney Life Aid, focusing on evaluation and improvement. I reviewed the final MVP function choices, explained the testing scope, and summarised  Think Aloud from classmate and tutor testing. The blog shows that a working prototype still needs user testing, interface refinement, clearer navigation, better search logic, and future improvements.
tags:
  - User Testing
  - MVP Evaluation
  - Iteration
---
## Evaluation of applications - Test analysis and summary

### Classroom Learning and Gains

In Week 11, I learned that finishing the prototype does not mean the system is already successful. We still need to check whether it works technically and whether real users can complete the task without confusion. For Sydney Life Aid, this means testing routes, database actions and HTMX updates, but also watching users through task-based testing and Think Aloud. I also realised testing and analytics should help us improve the task pathway, also we need protecting users’ privacy.

### Part Two: Final Function Selection and Implementation

![](assets/images/6.1.png)

In this section, we reviewed what should be retained in the final Minimum Viable Product (MVP) and what should be moved to the future expansion scope. We made this decision because the prototype needs to be testable and cannot have too many functions. We placed features such as automatic recommendations, complex notifications, and multilingual translation in the future scope. The screenshots show the current prototype being used, and we can now apply it for user testing.

### Part Three: Evaluation Plan and Test Scope
![](assets/images/6.2.png)

In this part, we planned how to test the prototype before treating it as finished. We divided the evaluation into several areas: core task flow, content clarity, interaction functions, database integrity, HTMX partial updates, accessibility, safety, and future scope. We did this because the website needs to be tested from both user and system sides. Users should be able to understand the task, find places, read posts, publish content, and return to settings without confusion. At the same time, login, search, save, like, comment, database records, and page updates must work reliably. This plan helps us find problems, and decide what to adjust next.

### Part Four: Classroom Test Feedback and Revision Directions

In the classroom test, we invited other group members to conduct "think aloud" and also had the tutor perform a functional test. The overall feedback was that the website direction, page content and functional logic were basically clear, and users could understand that this was a platform that helps Chinese international students find medical assistance and view their peers' experiences in Sydney.

However, the test also revealed several issues. Firstly, the login / user creation interface was somewhat cumbersome, with too much information to fill in, which might increase the burden for first-time users. Therefore, we plan to simplify the login process. Secondly, the navigation bar lacks a clear active state. Users expect that every time they switch to a new page, the navigation bar will have a color change indicating the current page. This would make it easier for them to determine which page they are on, so we will add the current page status. Thirdly, the search function is too strict. If a user inputs a long sentence but contains keywords, the system should also be able to find relevant posts. We will fix these issues in the future.

### Personal Reflection

In this final blog post, I have reviewed the entire process of transforming "Sydney Life Assistance" from an idea into a complete core minimum viable product (MVP). I realized that the most important thing was not to add more features, but to keep the core task path clear: entering the task, reading peer experiences, finding the location, saving useful information, and publishing or commenting. For the next stage, we still need to improve the interface based on the results of user testing. In terms of code, we need to improve CSS consistency to make the code cleaner and more organized. In the future, we hope to continuously improve the "Sydney Life Aid" platform so that it can become a more reliable support tool for Chinese students seeking medical treatment in Sydney.

#### Division of labor
Joint discussion and finalization. All charts and codes are jointly created and implemented.
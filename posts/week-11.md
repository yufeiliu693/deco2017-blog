---
title: Testing the MVP and Planning the Next Iteration
date: 2026-05-14
author: Yufei Liu
summary: This blog reflects on the Sydney Life Aid, focusing on evaluation and improvement. I reviewed the prototype, explained the testing scope, and summarised  Think Aloud from classmate and tutor testing. The blog shows that a working prototype still needs user testing, interface refinement, clearer navigation, better search logic, and future improvements.
tags:
  - User Testing
  - MVP Evaluation
  - Iteration
---
## Course learning gains

In the week 11, I learned that after completing the prototype, we still needed to check whether it was technically feasible and whether real users could complete the tasks without confusion. This meant we had to test the routes, database operations and HTMX updates, and also observe the users' performance through task-based tests and "meditative tests" to identify the problems they encountered during actual operations. And when collecting more private data from users in the future, we must pay attention to protecting user privacy.

## Part 1: Final Function Selection and Implementation

![](assets/images/6.1.png)

In this section, we discussed which elements should be retained in the final Minimum Viable Product (MVP) and which ones should be included in future expansions. We made this decision because the prototype needs to be testable and should not contain too many functions. Functions such as automatic recommendations, complex notifications, and multilingual translation are placed in the future expansion scope. Screenshots show the current situation in which the prototype is being used, and now we can apply it for user testing.

## Part 2: Evaluation Plan and Test Scope
![](assets/images/6.2.png)

In this section, we have developed a plan for testing the prototype before considering it as a final product. We have divided the evaluation into several aspects: core task flow, content clarity, interaction functions, database integrity, HTMX partial updates, accessibility, security, and future scope. We have divided the tests into two aspects: user and system. For the users, they should be able to understand the tasks, find the locations, read the posts, post content, and return to settings without confusion. For the system tests, login, search, save, like, comment, database records, and page updates must operate reliably. This plan helps us identify problems and determine what needs to be adjusted next.

## Part 3: Classroom Test Feedback and Revision Directions

In the classroom test, we invited other group members to conduct "think aloud" and also had the tutor perform a functional test. The overall feedback was that the website direction, page content and functional logic were basically clear, and users could understand that this was a platform that helps Chinese international students find medical assistance and view their peers' experiences in Sydney.

However, the test also revealed several issues. Firstly, the login / user creation interface was somewhat cumbersome, with too much information to fill in, which might increase the burden for first-time users. Therefore, we plan to simplify the login process. Secondly, the navigation bar lacks a clear active state. Users expect that every time they switch to a new page, the navigation bar will have a color change indicating the current page. This would make it easier for them to determine which page they are on, so we will add the current page status. Thirdly, the search function is too strict. If a user inputs a long sentence but contains keywords, the system should also be able to find relevant posts. We will fix these issues in the future.

## Personal Reflection

In this final blog post, I have reviewed the entire process of transforming "Sydney Living Assistance" from an idea into a prototype. I realized that the website's smooth usability is the most important thing. Therefore, throughout the entire process, continuous testing and communication with users is something that needs to be consistently carried out. For the next stage, we still need to improve the interface based on the results of user testing. And we also need to continuously be responsible for user security and privacy. 

In the future, we hope to continuously improve the "Sydney Life Assistance" platform, making it a more reliable auxiliary tool for helping Chinese students receive medical treatment in Sydney.

### Core design decisions:
We adjusted the subsequent optimization direction based on the feedback from the classroom tests.

### Division of labor
Joint discussion and finalization. All charts and codes are jointly created and implemented.
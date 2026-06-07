---
title: Sydney Life Aid Evaluation & Reflection
date: 2026-06-07
author: Yufei Liu
summary: A final reflection on the performance, user experience, accessibility, functional requirements, and future improvements of the Sydney Life Aid web application.
tags:
  - Web App Evaluation
  - User Experience Testing
  - AI testing
---
# Final Reflection: Evaluating Sydney Life Aid

## Introduction

Sydney Life Aid is a task-oriented community hub built around the real-life task "See a doctor in Sydney". Its target users are Chinese international students who feel uncertain about GP, pharmacy, emergency, OSHC and appointment processes. Built with Mojo.js, TypeScript, SQLite, HTMX and an MVC structure, Through pages such as Home/Task, Address, Community, Post Detail, Release, Settings/Profile, it connects "understanding the process, finding the location, reading experiences, interacting and saving, and returning to personal content" into a complete path. 

![](assets/images/7.3.png)

This reflection evaluates whether the system is stable, usable, accessible, and whether our initial functional requirements were realistic.


## Performance and Technical Behaviour

From the perspective of technical behavior, Sydney Life Aid performed reliably in the basic running and testing process. The project passed npm install, npm run seed, npm run dev, local opening, normally accessible at http://localhost:3000. And navigation checking, with no obvious 404 or 500 route errors. This showed that the main pages and routes were connected correctly, rather than only appearing complete at interface level.

![](assets/images/7.4.png)

More importantly, we do not merely judge the success of the project based on the "page being able to open". We also tested code quality and technical behaviour through npm run lint, npm run check and npm run test. tests/model.test.mjs checked user, task, post, comment, like, saved place and permission logic, while tests/routes.test.mjs checked whether the main page routes and action routes were registered correctly. This means stability was checked at both model and route levels, not only through manual clicking.

![](assets/images/7.5.png)

HTMX is a key technology that affects performance and interaction quality. Operations such as Like/Unlike, Comment, Reply and Save/Unsave Place can update through partial refresh instead of full-page reloads, making Community, Post Detail and Address feel lighter. Release and Comment forms were also tested with empty or incomplete input. The system did not crash, prompts appeared when needed, and empty data was not saved incorrectly, showing basic error prevention.

![](assets/images/7.6.png)

The Open-Meteo Weather API was placed in the service layer and passed by the controller to the Address page. This avoided mixing API logic directly into templates and allowed the page to remain usable even if API data temporarily failed. However, the performance evaluation was still limited because Network loading checks were mainly local. They showed no obvious waiting or resource failure, but did not fully represent slow networks, multiple users or server pressure in a real deployed environment. Image upload also needs future optimisation. The Release page supports preview, file type restriction, 2MB file size limit and maximum 9 images, but future versions should add compression, loading states and clearer upload feedback.

![](assets/images/7.7.png)


## User Experience and Accessibility

The user experience assessment is the most conclusive way to determine whether Sydney Life Aid has truly solved the problem. Our test subjects were three Chinese international students or people familiar with the life of international students. The testing methods included scenario-based testing, task-based usability testing, Think Aloud, and post-test interviews. The test scenarios were: the user was unwell in Sydney and needed to learn through the website how to see a doctor, where to go, what to prepare, and whether other students had similar experiences. 

![](assets/images/7.8.png)

The test results show that all three users were able to understand that this is a platform that helps international students see a doctor in Sydney, and they were also able to complete the core path of "Home → Address → Community". Home / Task, Address, Community and Settings / Profile together supported the full path from understanding the process to finding places, reading peer experiences and returning to saved personal content.

However, testing also revealed usability problems. Rebecca felt the Login page did not clearly show the website theme, so users might not understand the platform value before entering. YD found the Google Maps button not prominent enough, showing that key action buttons need stronger visual hierarchy. WQ felt there was too much text, which made reading burdensome. These issues are not small visual preferences; they affect whether users can act quickly when they are stressed, unwell or unfamiliar with the medical system. They also show that we prioritised complete information but did not compress or layer it enough.

![](assets/images/7.10.png)
![](assets/images/7.11.png)

In terms of accessibility, the prototype passed all key checks, including Lighthouse, contrast, keyboard navigation, focus status, form labels, image alt text, screen reader, and semantic HTML. Lighthouse reported no serious accessibility errors, contrast met readability requirements, keyboard navigation and focus states worked correctly, and the main forms had clear labels. Also the semantic elements such as header, nav, main, section, form, and button supported clearer navigation.

![](assets/images/7.12.png)

However, this test also made me realize that a high automated accessibility score does not necessarily mean a completely effortless real experience. WQ mentioned that "too much text" is actually a cognitive accessibility issue. For the target users, the medical process itself is already complex, and the interface should not add an additional burden on understanding. Therefore, the next step is not only to continue maintaining technical accessibility, but also to reduce the text density, using icons, step images, short labels, and progressive disclosure to help users quickly find the next step.

## Functional Requirements Reflection

Looking back at the initial functional requirements, I believe that the project has fulfilled the most crucial requirements overall, and the scope control is clearer than in the early stage. The core requirement is not to create a medical community with many functions, but to help users complete the task of "See a doctor in Sydney". The final prototype kept the core functions: task pathway, place information, peer experiences, Post Detail interaction, Release publishing, saved places, likes, comments, replies, profile management, language switching, weather information and responsive layout.

![](assets/images/7.13.png)
![](assets/images/7.14.png)

These functions are not isolated from each other. task_steps connects Home pathway cards, Community filters, Release step selector, post cards and peer_experiences.step_id. places connect Address page, Post Detail page and saved_places. peer_experiences links user experiences, locations, comments, likes and saving behaviors. This data structure makes the website not a "stack of pages", but a system built around a real task. 

![](assets/images/7.3.png)

At the same time, we have consciously redefined some functions. For instance, the project did not incorporate the complete Map API but instead initially used place cards and Google Maps external links; it did not include real-time chat, notifications, user levels, or complex recommendation systems. This is not a failure but a matter of scope determination. If too many functions are pursued within a limited time, the core process may become unstable. Ultimately, we prioritized ensuring that users can understand the process, find locations, read experiences, save information, and post content.

![](assets/images/7.1.png)
![](assets/images/7.2.png)

## Lessons Learned and Future Improvements

Through this project, My main lesson was that full-stack web quality depends on the consistency between user actions, data structure, backend logic and interface feedback. I mainly worked on backend logic, community interactions, save/unsave states, Settings updates, image upload and Release form interaction. This helped me understand that one button may involve template, route, controller, model, database query and HTMX response. Effective debugging means following the data flow, not only looking at the visible page. AI was used only as a support tool for code review, debugging and testing organisation, while final decisions and evaluation remained our own.

I also learned that form functionality is part of user experience. Image preview, file type restriction, file size limit, maximum 9 images, cover selection and required fields all affect whether users feel safe publishing content. If these details are weak, users may upload wrong files, submit empty content or be unsure whether the system received the action.

Future work should redesign the Login page, enlarge the Google Maps button, visualise the task steps, add upload compression and loading states, and retest performance in a real deployed environment.

The ultimate value of Sydney Life Aid lies not in the number of functions it contains, but in the way it organizes an originally vague, anxious and scattered medical assistance process into a web system that can be completed step by step. It has accomplished its core task, but the tests have also reminded me that a truly excellent web application is not just something that can run; it must also make the next step clear, trustworthy and actionable when the user needs help the most.

## Additional Evidence: AI Support and Testing Process

These two files provide supporting evidence for my final reflection: one records AI support during development and testing, and the other documents the full testing process.

- [AI Support and Prototype Testing Evidence](https://drive.google.com/file/d/1ltcNttOS24i8r1Vs5I15XodBI5PUE8X2/view?usp=sharing)
- [Full Testing Process Evidence](https://drive.google.com/file/d/1P6m1wfXkBVDK7yd4KSP_ShjShsZDdbvj/view?usp=sharing)
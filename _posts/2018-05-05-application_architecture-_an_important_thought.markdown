---
layout: post
title:      "Application Architecture- An Important Thought"
date:       2018-05-05 16:30:21 +0000
permalink:  application_architecture-_an_important_thought
---


Software development nowadays is about making diferent pieces of software work together. There is usually no thought given to architecture and when application grows, there are complex dependancies of one component to another. The affect of one change becomes costly. This is especially true of startup environments where it is very common to keep one repository. All changes happen on Master branch. When company starts gowing in size, it becomes difficult for Dev/Tech leads to manage merge conflicts. 

The time wasted on merge conflicts could've been better utilzed if the architecture was given a thought from the begining. One change to one component can bring entire system down. None of the teams are to be blamed when the release cycle looks like the following:

* Development Thurs-Friday (**6.5 days**)
* Code Freeze (Friday at Noon, 12pm EST)
* Code Review (Friday Noon- Friday night)
* Release Candidate/ Unit tests available (Sunday)
* Deployment to QA environment (**9am EST**)
* QA Testing on QA environment (**Monday-Tuesday**)
* Bug Fixing of defects found during QA (**Monday-Tuesday**)
* Bug Freeze (**Tuesday, 6pm EST**)
* Regression on QA Environment (**Wednesday 9am-12pm EST**)
* Deployment to Pre-Prod Environment (**Wednesday 12pm EST**)
* QA Sign-off (**Wednesday, 6pm EST**)
* UAT Sign-off (**Pre Thursday**)
* Deployment to Production (**Thursday 6:30 PM EST**)

                                                      **This is what two week sprint in Agile Environment looks like. **

Looking at how tight the schedule above is, thoughts given to architecture becomes obselete and more concentration is spent on how to make the release go. Usually developers like to develop on their local environment and then deploy to QA/Dev Environment then all of Pull requests are created. When Pull requests are merged, merge conflict resolution comes into play. Once  merges are resolved, the Release Candidate is deployed for QA team to test. Dependency on different components(Database, Data, Environments, etc) is not even highlighted in this release schedule. What if Database in Pre-Prod environment is down or didn't get synced with the latest data or QA Environment had old data where testing was conducted?. There are lots of thoughts that happens during this two week period. What would one week release schedule/timeline would look like? How complex dependencies of different components or complexity of Architecture will play out?. Team should sit down and start thinking about this but when?. There is no time as many companies are delivery driven. Clients are waiting eagerly on the components which they wanted added to their reports/UI. What about bug fixes? That's really an interesting thought. Bugs can arise for many different reasons(Environment related, Data related and software related). Looking at all of this moving pieces(Business Priority, Tech Priority, Client's happiness) strong architecture must be the priority. It helps in the long run as making changes, resolving merge conflicts becomes easier and end-users get what they want in timely manner.

---
layout: post
title:      "Leads Management Using Ruby on Rails"
date:       2018-08-01 02:33:54 +0000
permalink:  leads_management_using_ruby_on_rails
---


This is an iteration of the Leads Management System using Sinatra. The app now runs on Ruby on Rails and has some improvements over the one implemented in Sinatra.

This app lets different users or agents track and manage his/her leads - potential customers. An agent signs up or signs in, and then track his leads which hopefully will be converted as sales. There are CRUD funcitonalities for managing the leads. Different agents can track their respective leads but not see the leads of other agents. The agent though can see the leads in his region and the leads in a particular industry. He won't know though who those leads belong to. If an agent signs up as a manager, the manager can see how each region is doing and how each industry is doing. He can also see how agents in his/her region are doing.

Notable improvements are the following:
1. Sign in Using Facebook - A user can now access the app by using his/her Facebook account.

2. Manager type as User - There is now a manager for a particular region where that manager can have his own leads and at the same time see the performance of agents in his assigned region. He also has other access privileges that a regular agent doesn't have like see how all regions are doing, see how all agents in his region are doing, and see how all industries are doing.

3. Filtering of Leads by Status - An agent can now filter leads according to Status.

4. Use of CSS - This app is better in appearance compared to the app using Sinatra.

This project took almost a week to complete. Main issue was the scoping of the project. There were times I thought I should be putting in more features which led to more code and more complexity for the user. There was a lot of time spent in planning and selecting which features to incorporate. The last day of the project was spent refactoring the code and styling using CSS. 

See the project here: https://github.com/ktamoguis/model-class-methods-lab-v-000 


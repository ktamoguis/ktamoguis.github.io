---
layout: post
title:      "Sinatra Project: Leads Management System"
date:       2018-07-03 00:50:13 +0000
permalink:  sinatra_project_leads_management_system
---


This project is an MVC Sinatra App which tracks/manages leads (or potential customers) of sales agents located in different regions.  As a sales agent, one can create and keep track of one's leads. The sales agent can update the status of the lead depending on how far or how near the lead is going to be converted or eventually become a customer. Also, the sales agent can see a summary of leads per region and their corresponding status. He can see a detailed list of leads and their status in his region but not those in other regions.

The project took around 4 days to complete. The first day was mostly ideation, what the project will be like. I also tried to visualize the user experience: what kind of views the user or in this case, the sales agent, will use. Second day was dealing mostly with technical issues with my local terminal. I ended choosing to do the project in Learn's IDE because I wouldn't have to worry about gem installation in my computer. The third and fourth day was mostly coding and testing and then finishing touches.

One realization that came to me was how much I would depend on using shotgun in testing my code. When I was doing the labs, I mostly relied on the test results to help me finish the app. I did use Shotgun but not as much as I did when developing this project. Everytime I tried to do write some code, I would almost immediately use shotgun to try out the app. Of course, there's also binding.pry. I would heavily rely on thse two gems until I completed the project.

After more or less the workflow for using the app was coded, I put in the validation measures which would check whether a field is missing, or if a particular agent name or region name already exists. While doing this, I also tried to do some styling with how views will be rendered.

Main challenge for me was trying to think of all the different scenarios a user of the app might experience. In each case, I needed to think of validation measures and how the app will proceed. This took almost the same time as coding the workflow of the app.

App can be found here: [https://github.com/ktamoguis/sinatra-cms-app-assessment-v-000.git]


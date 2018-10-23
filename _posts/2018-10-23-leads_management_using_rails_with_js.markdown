---
layout: post
title:      "Leads Management using Rails with JS"
date:       2018-10-23 17:39:23 -0400
permalink:  leads_management_using_rails_with_js
---


This project is the latest iteration of the Leads Management System. It all started with using [Sinatra](https://ktamoguis.github.io/sinatra_project_leads_management_system), then [Rails](https://ktamoguis.github.io/leads_management_using_ruby_on_rails) and now using Rails with Javascript. As the project has gone through these iterations, I've added several useful features:



**1. See Index of Leads without page refresh**

When the user is in the agent's show page, the user can see the list of leads the agent has without refreshing the page.



**2. See Leads Show page without page refresh**

Still in the agent's show page and after loading the index of leads the agent has, the user can click on each lead and see more details for the said lead. The user can also click the 'Next' button to display the details of the next lead.



**3. Add Owners to a Lead**

The user can go the leads show page - not using JS - by typing in /leads/:id and add owners to the lead. The user has just to fill up text box with the owner's name and after pressing the Create Owner button, the page will automatically update without page refresh.


The project took almost a week to complete. The first two features were done in a couple of days. The last feature took the longest because of a persistent bug. When creating an owner, the page wouldn't automatically add the new owner to the page. Also, the Create Owner button, would remain disabled after pressing it. The user had to refresh the page to update the page and to re-enable the Create Owner button.

For the first problem - not automatically adding the new owner, I overlooked that when serializing the owner, the serialized data came with id and name. I was appending the data without specifying which part of data I wanted to append. In this case, data.name. Also since the new owner would be appended to an ordered list (ol), I forgot I had to specify `<li>` when appending

```
posting.done(function(data) {
        $("#owner_name").val("")
        var $ol = $("div.owners ol")
        //$ol.append(data) - code before
        $ol.append(`<li>` + data.name  + `</li>`) // code after
```


For the part where the Create Owner is not re-enabled after pressing, I just had to manually re-enable it using some code.

```
posting.done(function(data) {
        debugger;
        $("#owner_name").val("")
        var $ol = $("div.owners ol")
        //$ol.append(data)
        $ol.append(`<li>` + data.name  + `</li>`)
        $( "input[value='Create Owner']" ).prop('disabled',false); //code to re-enable the button
      });
```
			

Here's the [link](https://github.com/ktamoguis/leadsmgt_js) to the project.
			


# Holiday Planner: a programmer exercise <sup>[![Version Badge]</sup>

[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

This repo is just a programming exercise, you can use it for job interviews or just during a speech, 
talking about code best practices (like us).

The task consist in designing a basic Web Application for holiday planning.
The developer will realize the follow building blocks:
 * a Web Application using a Javascript Framework (we suggest React)
 * a backend Rest API application using PHP or Java (se suggest Symfony 4)
 * a relation database in order to persist data (we suggest MySQL)
 
## The scenario

The web application should simplify planning and managing holidays in your company.
In the basic version the user should e able to:
 * see the list of all requested holidays
 * insert a new holiday request
 * open the detail
 * mark a request as "Approved"
 
Each holiday is made by  the following fields:
 * employee
 * start
 * end
 * note
 * businessUnit
 * responsible1: name of the first responsible for this employee
 * approvedBy1: whether or not the first responsible has approved the holiday
 * responsible2: name of the second responsible for this employee
 * approvedBy2: whether or not the second responsible has approved the holiday

### List of holiday requests
 
In the Home Page the user expects to find a list of all holiday requests. In the table you should visualize the following
fields: employee, start, end, businessUnit, note (only the first 30 chart followed by dots ..., if it’s longer),
approved ("yes", "no", "partially" if it's respectively approved by both the responsible, none, only one).

**TODO: add screenshot**

### Add new holiday request

The user can insert a new holiday request by clicking on "Add" in the top bar. 
In the "New holiday request" page the following data are required:
- employee: choice limited between a few elements, you can invent some employee names
- start
- end – must be later than the start (bonus if the app warns that there is overlapping: a user of the same business unit 
is requesting holiday with overlapping dates)
- note
- businessUnit: choice limited between a few elements - You can invent 3-5 values.
- responsible1: choice limited between a few elements. You can invent 5-10 names
- responsible2: choice limited between a few elements, the user can't choose the same element for 
both responsible1 and responsible2

**TODO: add screenshot**

### Edit existing holiday request

Back on the home page, the user can click on any holiday request and see the details. 
It's possible to do the following changes:
 * change the "note" field
 * approve the revision on behalf of the responsible (can only approve it, can’t be "disapproved")

**TODO: add screenshot**

## Suggestions

It's just an exercise, so you don't need to overcomplicate it!
You can avoid to implement the following features/requirements:
 * login
 * user profiles/roles
 * pixel perfect UI

## Sample projects

You can find my demo project in my github: 
* matteogll/holiday-planner-sym4-api: API and database
* matteogll/holiday-planner-react-fe: React frontend

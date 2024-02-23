<br>
<small>CIS2169 | <b>Web Design and Development</b> | Department of Computer Science | <b>Edge Hill University</b> </small>
<br>

---

# CIS2169  🎓 Academic Management System 💻

This development container has everything you will need (`javascript`, `NODE.js` and `JSON-Server` and various VS Code extensions) to implement your solution for assessment 2. 

## Overview

Below is a summary of the *default* contents:

* `.devcontainer` : This directory contains the configuration for this container. Please do not modify.

* `json-server` : This directory is where you will place the neccessary files to simulate database requests via a REST API. The *default* contents of this directory contains the example [Pokemon Rest API](https://github.com/Edge-Hill-University-Web/Pokemon-Json-Server). You will need to modify the contents to reflect your designs and implementation for this assessment.

* `app` : Clone **your** forked repository into this directory. This is where you will develop your solution.

## Getting Started with your assessment

To begin this assessment you will need to first need to fork the [Original Academic Management System](https://github.com/Edge-Hill-University-Web/CIS2169-Academic-Management-System-2023-2024) repository and then familiarise yourself with [Scenario](https://learningedge.edgehill.ac.uk/ultra/courses/_302616_1/outline/edit/document/_5402621_1?courseId=_302616_1&view=content) documentation. Using both these resources you are to then model and implement the extended features. More detailed information regarding this assessment can be found on Blackboard.

## JSON Server

Rather than you implementing a Database, you will be required to use `JSON-Server` to simulate backend functionality. `JSON-Server` allows you to create a REST API with endpoints, routes and more to access your simulated data. This is achieved by creating various JSON files. For your convenance a template of these various files can be found in the `json-server` directory. 

Inside the `json-server` directory there are:

* `data` : This houses everything required to mock the data, define endpoints and more
  
  * The `public` directory contains the files for the Json-Server's landing page.

* `routes` : This contains the `routes.json` file. This file is where you will define your routes. 
* `data.json` : This contains all the mocked data you require for you application.
  
<br>

More information about `JSON-Server` can be found [here](https://github.com/typicode/json-server). 

If you would like to see an example of how this can be used I suggest taking a look at [Pokemon REST API](https://github.com/Edge-Hill-University-Web/Pokemon-Json-Server) GitHub repository.

### Launching JSON Server
Ensure you are the root directory of the workspace (`/workspaces/`) and run the following command in a **new** bash terminal (within the container!) to launch **JSON Server**:

```bash
json-server  -w json-server/data/data.json --routes json-server/data/routes/routes.json --port 80
```
Remember, that the instance of `Json-Server` is running inside your container. Therefore it is accessible via the `localhost` of the container via port `80` (`localhost:80`). Note, upon a successfull launch, this should automatically open the `Json-Server`'s landing page in your default web browser. This can be useful for testing and debugging. 

Below is some example code to get you started. Note this will work with the *default*
`data.json` and `routes.json` files.

 ```javascript
fetch(" http://localhost:80/trainers")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
and should return the following list of `trainers` in json format:
```json
[
  { id: '001', name: 'Dan', route: '4' },
  { id: '002', name: 'Harley', route: '3' },
  { id: '003', name: 'Leia', route: '3' }
]
```
<br>

## ⚠️ Application Submission Guidance ⚠️ 
When submitting your application remember to also include the `json-server` directory and contents to. Otherwise, your mocked data will not be available when it comes to marking.

You have been warned.
<br>
<br>
<br>
<br>

---

# Instructions: Readme

Here is where you will define the instructions for running your application. Remember to include information on how to install any dependencies you have used. You do not need to include instructions on how to deploy the container! Just what is required to run your application.

---
<br>
<small>
CIS2169 | <b>Web Design and Development</b> | Department of Computer Science | <b>Edge Hill University</b> </small>



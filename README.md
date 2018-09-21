## <a href="https://github.com/rhildred/razordotnetcorepages" target="_blank">Model View Controller (MVC)</a>

### Assignment 9

![Northern Threads](https://res.cloudinary.com/salesucation-com-inc/image/upload/v1522973943/NorthernThreads750x500_zt8i5q.png "Northern Threads")

Sometimes as developers we make or are given a prototype to turn into an app. Your task is to turn the prototype at  [https://github.com/hexx0960/NorthernThreads/](https://github.com/hexx0960/NorthernThreads/)  into a .net mvc application.

You can see the .html prototype in action at  [https://hexx0960.github.io/NorthernThreads/](https://hexx0960.github.io/NorthernThreads/). It has 13 pages which you will turn into controller based routing. For more marks you can put the clothing products on the web site into a database. Finally you can implement the buy now button and the shopping cart.

To do this assignment you will need one important design pattern and some technical details to back it up.

### Separation of concerns

![picture from 1988 essay](https://rhildred.github.io/razordotnetcorepages/readmeimages/mvcFrom1988Article.png "picture from 1988 essay")
picture from Glenn E. Krasner and Stephen Pope's 1988 essay in JOOP - Journal of Object-Oriented Programming

The design pattern is from a 1988 essay. The idea is that if you separate business logic and data from display of data and user input you can easily have multiple views of the same data. In our application we have categories, separating our views. Men's, Women's and accessories. 

### Multiple views of the same data

![web monitoring app](https://upload.wikimedia.org/wikipedia/en/a/a7/Octopussy-v09-RRD-Graph-2007.png "web monitoring app")
License: CC-BY-SA-3.0 granted by Sebastien Thebert on 2017-04-07.

Another place where we see multiple views of the same data is when considering a graph and table of the same data. Here we have a web monitoring app with the table providing a key for the graph above it.

The model view controller predates the web by a few years. When the pattern was applied to the web the views were generated from model data by templates. .net MVC uses razor templates to present the model as .html. Web MVC also includes technology independent/SEO friendly URLs.

## Razor Web Pages
### The razor syntax is independent of MVC

![a chatbot](https://rhildred.github.io/razordotnetcorepages//readmeimages/chatbotweb.png "a chatbot")

The current Microsoft recommended way of making simple web sites is "Razor Web Pages". A razor web page is a code behind page. The markup is written in .cshtml. The code behind in .cshtml.cs.

## Razor uses @ and @{}

![code behind](https://rhildred.github.io/razordotnetcorepages/readmeimages/FileLayout.PNG "code behind")

![@RenderBody](https://rhildred.github.io/razordotnetcorepages/readmeimages/Layout.PNG  "@RenderBody")

There is also a layout page for things like scripts, css that repeat on every page. If you need an actual `@` sign use `@@`

## Twilio webhook

![OnPost](https://rhildred.github.io/razordotnetcorepages/readmeimages/OnPost.PNG "OnPost"))

The razor web pages, like webforms are a quick way of getting a dynamic page or webhook on the internet. 

## Web Input Routing CRUD
### 4 types of request in common use

|Http verb|CRUD|SQL|
|---|---|---|
|POST|Create|INSERT|
|GET|Read|SELECT|
|PUT|Update|UPDATE|
|DELETE|Delete|DELETE|

REpresentational State Transfer ... "
Roy Fielding defined REST in his 2000 PhD dissertation "Architectural Styles and the Design of Network-based Software Architectures" at UC Irvine." (Wikipedia) We use the http verbs in our routes one way or another.

## Page based routing
### What you should already be used to

![page base route](https://rhildred.github.io/razordotnetcorepages/readmeimages/PageBasedRouting.PNG "page base route")

Here we see a page `Results.aspx`. .aspx is a giveaway to the technology being used. Additionally we have a query parameter after the question mark.

## Friendly URL based routing
### independent of the technology used

![Mens#Suits](https://rhildred.github.io/razordotnetcorepages/readmeimages/MensSuits.PNG "Mens#Suits")

The first thing that I want you to notice about this is the URL. Rather than ending in .aspx or .cshtml it is just /Mens. Am I right. Not quite. The url ends in #Suits. The #Suits part is for the browser to go to the #Suits section of the page. Browser routing. The server side routing ends at /Mens.

## MVC blamed for lots of little files.

![lots of little files](https://rhildred.github.io/razordotnetcorepages/readmeimages/MVCLayout.PNG "lots of little files")

In our app we are just replacing repetitive .html files with .cshtml files that only contain what is different about the page. The shared parts of the page are in the Shared folder in the _Layout.cshtml file.

## The routes are defined in the controller

![controller](https://rhildred.github.io/razordotnetcorepages/readmeimages/Controller.PNG "controller")

This one is the home controller so /Home/Mens, /Home/About ....

## Friendly URL routing can also be technology independent

![friendly routes](https://rhildred.github.io/razordotnetcorepages/readmeimages/FriendlyRoutes.PNG "friendly routes")

It is also possible to make the routes be whatever you want them to be using the nuget Microsoft.AspNet.FriendlyUrls.Core package.






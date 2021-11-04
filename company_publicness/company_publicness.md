## Problem: Is this company public?

At AlphaSights, when we consider using an expert for a project, we are careful to record the companies they have worked for in the past. This is important as some of our clients have restrictions on whether the experts they engage with have worked in publicly listed companies. In order to determine whether a company is publicly listed we refer to an external data set. 

Data coming from the external data set keeps track of company hierarchies. 
We deem a company public if there is at least one public company in its hierarchy, see example below:


If Google UK is marked as a public company, all companies within that hierarchy would be considered public as well (the reverse would also be true - if it’s Alphabet that is marked as public it would deem all the companies in that hierarchy public as well).


## Task 1
Write an algorithm which given a company object will return a boolean value of its publicness. 

Company class
parent : Company;
children : List<Company>
name : String

isPublic(companyName: String, rootNode, publicCompanyNames: Set<String>) : boolean

Would return true for every company in the hierarchy above.


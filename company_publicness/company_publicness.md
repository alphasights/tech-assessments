> This problem has been added to the Questions Library in Coderpad, so for the interview, it can be selected directly from the Questions tab, and the candidate will view this file in the `Instructions` tab on the right panel.

# Problem: Company Publicness
At AlphaSights, when we consider using an expert for a project, we are careful to record the companies they have worked for in the past. This is important as some of our clients have restrictions on whether the experts they engage with have worked in publicly listed companies. In order to determine whether a company is publicly listed we refer to an external data set.

Data coming from the external data set keeps track of company hierarchies and which ones are Public. We deem a company public if there is at least one public company in its hierarchy, see example below:

           Alphabet
        /      |    \
    Google   Google   Google
       US    Mobile    UK
             /    \
        Android   Waze
      
  
So if any of these Companies has `public=True`, we consider them all to be Public. E.g.: If "Google Mobile" is marked as a public company, all companies within that hierarchy would be considered public as well. If it’s Alphabet that is marked as public, it would deem all the companies in that hierarchy public as well.


## Task 1:
Write an algorithm which given a Company object it returns a boolean representing if we consider it internally as a Public company.
```bash
isPublic(company: Company) : boolean
```

## Follow up questions
1. How would you store company hierarchies in the database?
2. Considering there are huge hierarchies, how would you improve performance of the publicness calculation? 
    * Caching publicness value per company, refreshing when hierarchy changes
    * In most cases it is ultimate parent that is public - storing link to ultimate parent for every entity and checking it first might improve most of the queries


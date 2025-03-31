
```dataview
TABLE  WITHOUT ID
("<img src='" + cover + "' width='80px'/>") as "Cover",
file.link AS "Title",
author AS "Author",
status AS "Status", 
finished AS "Finished", 
rating AS "Rating",
series AS "Series",
level AS "English Level"
FROM "Books"
SORT series ASC, number(order) ASC, file.name ASC
```

















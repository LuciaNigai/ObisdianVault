
```dataview
TABLE  WITHOUT ID
("<img src='" + cover + "' width='80px'/>") as "Cover",
file.link AS "Title",
author AS "Author",
series AS "Series",
status AS "Status", 
finished AS "Finished", 
rating AS "Rating"
FROM "Books"
WHERE series
SORT series ASC, number(order) ASC
```




































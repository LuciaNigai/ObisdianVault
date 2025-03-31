
```dataview
TABLE WITHOUT ID
  ("<img src='" + cover + "' width='80px'/>") AS "Cover",
  file.link AS "Title",
  author AS "Author",
  status AS "Status", 
  finished AS "Finished", 
  rating AS "Rating",
  series AS "Series",
  level AS "English Level"
FROM "Books"
WHERE contains(status, "Reading")
SORT series ASC, order ASC, file.name ASC
```





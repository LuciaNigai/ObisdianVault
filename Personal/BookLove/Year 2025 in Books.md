
```dataview
TABLE WITHOUT ID
  ("<img src='" + cover + "' width='80px'/>") as "Cover",
  file.link AS "Title",
  author AS "Author",
  status AS "Status", 
  finished AS "Finished", 
  rating AS "Rating",
  series AS "Series",
  level AS "English Level"
FROM "Books"
WHERE finished.year = date(today).year  // This filters the books finished this year
SORT finished DESC, series ASC, order ASC, file.name ASC
```




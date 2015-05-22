---
layout: post
title: Get row count for all tables in database
---

I find the need to get the row count for all tables of a database from time to time and I found a neat way of doing just that using this little code snippet =)

```sql

SELECT o.NAME, i.rowcnt 
FROM sysindexes AS i
  INNER JOIN sysobjects AS o ON i.id = o.id 
WHERE i.indid < 2  AND OBJECTPROPERTY(o.id, 'IsMSShipped') = 0
ORDER BY o.NAME
```

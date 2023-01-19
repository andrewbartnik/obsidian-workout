---
type: <% await tp.system.suggester(["Pull", "Push", "Legs", "Abs"], ["Pull", "Push", "Legs", "Abs"])%>
date: <% await tp.system.prompt("Date, DD-MM-YYYY") %>
---
```dataview
TABLE exercise, target, rec, pos
FROM ("Areas/Health/Exercises")
WHERE date = this.date
SORT pos ASC
```

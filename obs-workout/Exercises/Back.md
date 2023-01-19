---
date: {{VALUE:date}}
type: Pull
group: Back
exercise: <% await tp.system.suggester(["Pull Ups", "Dumbbell Rows", "Incline Dumbbell Reverse Row", "Cable Pulldowns", "Close Grip Cable Pull Downs", "Barbell Rows", "Cable Rows", "Lat Pulldowns", "Close Grip Lat Pulldowns", "Wide Grip Cable Rows", "Iso-lateral High Rows", "Iso Lateral Low Rows", "Single Arm Cable Pulldown", "T-Bar Row", "Iso Lateral Front Lat Pulldown", "Rope Rows", "Mid Rows", "Machine Rows"], ["Pull Ups", "Dumbbell Rows", "Incline Dumbbell Reverse Row", "Cable Pulldowns", "Close Grip Cable Pull Downs", "Barbell Rows", "Cable Rows", "Lat Pulldowns", "Close Grip Lat Pulldowns", "Wide Grip Cable Rows", "Iso-lateral High Rows", "Iso Lateral Low Rows", "Single Arm Cable Pulldown", "T-Bar Row", "Iso Lateral Front Lat Pulldown", "Rope Rows", "Mid Rows", "Machine Rows"]) %>
pos: <% await tp.system.prompt("Position") %>
target: <% await tp.system.prompt("Target sets/reps") %>
rec:
---

```dataview
LIST
FROM ("Areas/Health/Workouts")
WHERE date = this.date
```

```dataview
TABLE exercise, date, target, rec
FROM ("Areas/Health/Exercises")
WHERE exercise = this.exercise
SORT date ASC
```
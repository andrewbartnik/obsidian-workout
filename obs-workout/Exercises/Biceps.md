---
date: {{VALUE:date}}
type: Pull
group: Biceps
exercise: <% await tp.system.suggester(["Drag Curl Smith Machine", "Incline Hammer Curls", "Incline Alternating Curls", "Inside Grip EZ Bar Curls", "Outside Grip EZ Bar Curls", "Preacher Curls (Rotate Wrist)", "Incline Bench Hanging Curls", "Barbell Curls", "Seated Cable Curls", "Rope Curls", "Single Arm Cable Curls", "Crucefix Curls", "Concentration Curls", "Crush Grip Curls"], ["Drag Curl Smith Machine", "Incline Hammer Curls", "Incline Alternating Curls", "Inside Grip EZ Bar Curls", "Outside Grip EZ Bar Curls", "Preacher Curls (Rotate Wrist)", "Incline Bench Hanging Curls", "Barbell Curls", "Seated Cable Curls", "Rope Curls", "Single Arm Cable Curls", "Crucefix Curls", "Concentration Curls", "Crush Grip Curls"]) %>
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
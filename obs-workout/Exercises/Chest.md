---
date: {{VALUE:date}}
type: Push
group: Chest
exercise: <% await tp.system.suggester(["Bench Press", "Incline Press", "Dumbbell Press", "Dumbbell Incline", "Chest Press", "Decline Cable Chest Fly", "Incline Cable Chest Fly", "Incline Dumbbell Fly", "Decline Dumbbell Fly", "Seated Chest Fly", "Chest Press", "Iso Lateral Incline", "Iso Lateral Decline", "Dumbell Close Press", "Dips", "Pushups"], ["Bench Press", "Incline Press", "Dumbbell Press", "Dumbbell Incline", "Chest Press", "Decline Cable Chest Fly", "Incline Cable Chest Fly", "Incline Dumbbell Fly", "Decline Dumbbell Fly", "Seated Chest Fly", "Chest Press", "Iso Lateral Incline", "Iso Lateral Decline", "Dumbell Close Press", "Dips", "Pushups"]) %>
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
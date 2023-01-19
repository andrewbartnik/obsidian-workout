---
date: {{VALUE:date}}
type: Push
group: Triceps
exercise: <% await tp.system.suggester(["EZ Bar Skullcrusher", "Dumbbell SkullCrusher", "Overhead Dumbbell Extension", "Overhead Cable Extension", "Single Arm Cable Extension (Overhand)", "Close Grip Bench", "Dips (Triceps)", "Tricep Cable Extension V grip", "Tricep Cable Extension Rope", "Triangle Pushups", "Dumbbell Kickbacks", "Tricep Cable Extension Bar", "Cable Tricep Kickback"], ["EZ Bar Skullcrusher", "Dumbbell SkullCrusher", "Overhead Dumbbell Extension", "Overhead Cable Extension", "Single Arm Cable Extension (Overhand)", "Close Grip Bench", "Dips (Triceps)", "Tricep Cable Extension V grip", "Tricep Cable Extension Rope", "Triangle Pushups", "Dumbbell Kickbacks", "Tricep Cable Extension Bar", "Cable Tricep Kickback"]) %>
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
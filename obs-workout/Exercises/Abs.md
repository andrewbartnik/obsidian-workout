---
date: {{VALUE:date}}
type: Abs
group: Abs
exercise: <% await tp.system.suggester(["Weighted Crunch", "Penguin", "Plank", "Side Crunches", "Ab Wheel", "Oblique Sit Up", "Superman", "Russian Twists", "Leg Raises", "Flutter Kicks", "Hanging Leg Raises"], ["Weighted Crunch", "Penguin", "Plank", "Side Crunches", "Ab Wheel", "Oblique Sit Up", "Superman", "Russian Twists", "Leg Raises", "Flutter Kicks", "Hanging Leg Raises"]) %>
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
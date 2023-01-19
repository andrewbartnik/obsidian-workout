---
date: {{VALUE:date}}
type: Push
group: Shoulders
exercise: <% await tp.system.suggester(["Dumbbell Shoulder Press", "Arnold Press", "Seated Lateral Raises", "Seated Front Raises", "Incline Bench Front Raises", "Wide Grip Barbell Shrug", "Dumbbell Front Delt Raise", "Steering Wheel", "Cable Rope Front Raise", "Side Lying Lateral Raise", "EZ Bar Upright Rows(Outer Grip)", "Leaning Lateral Cable Raise", "Face Pulls", "Cable Crossover", "Reverse Pecdec"], ["Dumbbell Shoulder Press", "Arnold Press", "Seated Lateral Raises", "Seated Front Raises", "Incline Bench Front Raises", "Wide Grip Barbell Shrug", "Dumbbell Front Delt Raise", "Steering Wheel", "Cable Rope Front Raise", "Side Lying Lateral Raise", "EZ Bar Upright Rows(Outer Grip)", "Leaning Lateral Cable Raise", "Face Pulls", "Cable Crossover", "Reverse Pecdec"]) %>
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
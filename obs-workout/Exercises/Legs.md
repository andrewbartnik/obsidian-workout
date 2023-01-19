---
date: {{VALUE:date}}
type: Legs 
group: Legs
exercise: <% await tp.system.suggester(["Bulgarian Split Squat", "Single Leg Glute Bridge", "Smith Machine Calf Raises", "Barbell Split Squats", "Glute Ham Raise", "Single Leg Calf Raise", "Hex Deadlift", "Squat", "Single Leg RDL", "Single Leg Press", "Ham Curls", "Leg Press", "Hack Squat", "Power Clean", "Hang Power Clean", "Barbell Good Morning", "Barbell Deadlift", "Romanian Deadlift", "Nordic Ham Curl", "Double Leg Landing", "Hex Bar Jump", "Seated Box Jumps", "Depth Jumps", "Rim Jumps", "Lunge Jumps", "Weighted Explosions", "Medicine Ball Approach", "Weighted Step-Up", "Depth Landings (Single Leg)"], ["Bulgarian Split Squat", "Single Leg Glute Bridge", "Smith Machine Calf Raises", "Barbell Split Squats", "Glute Ham Raise", "Single Leg Calf Raise", "Hex Deadlift", "Squat", "Single Leg RDL", "Single Leg Press", "Ham Curls", "Leg Press", "Hack Squat", "Power Clean", "Hang Power Clean", "Barbell Good Morning", "Barbell Deadlift", "Romanian Deadlift", "Nordic Ham Curl", "Double Leg Landing", "Hex Bar Jump", "Seated Box Jumps", "Depth Jumps", "Rim Jumps", "Lunge Jumps", "Weighted Explosions", "Medicine Ball Approach", "Weighted Step-Up", "Depth Landings (Single Leg)"]) %>
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
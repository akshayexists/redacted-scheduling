# Constraint-Bound Scheduling Framework

Built when I was a [redacted] at [redacted]

For when planning the task takes longer than the task itself.

Built using Google OR‑Tools [CP-SAT](https://developers.google.com/optimization/cp/cp_solver).

## Why?

 **Simple:** Tackles scheduling constraints Excel, Google Calendar, or your brain won’t touch, with zero effort on your part.

 **Flexible:** Any task type, any period, hard or soft deadlines, weighted tasks.

 **Ready-to-Use:** JSON config. Excel output. Zero code fiddling.

## Key Features

* Hard vs Soft deadlines per event
* Weighted tasks influencing penalties
* Configurable tie-break preference ("early" vs "late")
* Soft-deadline penalties to gently enforce timelines
* Excel output with **Deadline Status** column: "On time" or "Late (soft)"
* Handles reserved, public holiday, and unavailable periods
* Constrains consecutive and short-spacing repeats

## Possible Future Applications

* Manufacturing & production lines
* Employee shift planning
* Classrooms & exams
* Resource allocation & project timelines
* [redacted] scheduling that I initially wrote this for

## How It Works

1. **Load JSON:** Tasks, periods, constraints.
2. **Pack Schedule:** CP‑SAT handles hard rules.
3. **Refine:** Simulated annealing + tabu search smooth repetition.
4. **Soft-Deadline Handling:** Assigns weighted penalties for late soft deadlines.
5. **Tie-Break Preference:** Slight bias to schedule early or late periods.
6. **Export:** Clean Excel schedule, ready to act, with "Deadline Status" column.

## Quick Start

```cmd
python scheduling.py
```
edit data.json to your needs

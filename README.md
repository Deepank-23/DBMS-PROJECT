# IPL Match Simulation Database

A mini IPL-style cricket match simulation database built using SQLite and SQL.

## Features

* Team and player management
* Match and innings simulation
* Ball-by-ball data storage
* Cricket statistics queries
* Relational database design using foreign keys

## Technologies Used

* SQL
* SQLite

## Database Tables

* `team`
* `player`
* `season`
* `match`
* `inning`
* `over`
* `ball`
* `venue`

## Match Simulated

Mumbai Indians vs Chennai Super Kings

| Team                | Score |
| ------------------- | ----- |
| Mumbai Indians      | 27    |
| Chennai Super Kings | 28    |

**Winner:** Chennai Super Kings

## Sample Query

```sql
SELECT p.full_name AS Player, SUM(b.runs) AS Runs
FROM player p
JOIN ball b ON p.player_id = b.batsman_id
GROUP BY p.full_name
ORDER BY Runs DESC;
```

## How to Run

```bash
sqlite3 cricket.db
.read cricket_simulation.sql
```

## Learning Outcomes

* SQL schema design
* Foreign key relationships
* Aggregate queries
* Sports database modeling

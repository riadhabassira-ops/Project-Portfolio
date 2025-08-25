# Restaurant Simulation — MS210 Group Project (2022)

**Course:** MS210 Simulation Modelling  
**Type:** University group simulation project  
**Topic:** Fast-food restaurant operations — Simul8 model for queue, staffing, and utilisation optimisation.

## TL;DR
- Built a **Simul8** simulation for a 24/7 fast-food restaurant to analyse customer queues, staffing levels, and bottlenecks.
- Objective: **80% of customers wait < 5 minutes** while minimising staff cost & waste.

## Background
The project models a fast-food restaurant with eat-in, drive-through, and takeaway options.  
Key goals:
- Minimise customer wait times.
- Optimise staff scheduling across shifts.
- Reduce bottlenecks and food waste.

## Data Collection & Modelling
Inputs:
- Arrival rates (customers/hour by time of day).
- Staff processing times & rota constraints.
- Inventory deliveries (9am & 9pm).

Outputs:
- Queue wait times.
- Staff utilisation rates.
- Mean queue length.

Assumptions:
- Unlimited queue capacity (simplification for modelling ease).
- Normal arrival and service time distributions.
- 24/7 operation with 3 shifts/day.

Constraints:
- Limited staff space.
- Only 8–10 key activities to keep the model concise.

## Simul8 Model
- Customer entry points: Eat-in/Takeaway, Drive-through.
- Orders → Kitchen → Collection points.
- Deliveries twice per day.
- Shift-based staffing schedules.

Verification & Validation:
- Base model created with logical flow.
- Snapshots saved for experimentation phases.

## Experimentation & Recommendations
- Added a **second till** to reduce queue abandonment.
- Tested increased staff levels at peak hours.
- Suggested reducing **stock deliveries** to cut waste.
- Proposed improved queuing procedures for better flow.

## Results
- Adding a second till significantly reduced bottlenecks.
- Optimal staff rota found for peak vs off-peak hours.
- Lower stock delivery frequency improved profit margins.

## Next Steps
- Add customer feedback loops.
- Explore social media demand effects.
- Implement dynamic staffing rules.

## Project Structure
```
.
├── README.md
├── data/            # arrival rates, staffing data
├── simul8_model/    # Simul8 model files (.s8)
├── figures/         # screenshots of Simul8 flow & experiments
└── report.pdf       # final report if public sharing allowed
```

## License
MIT (adjust as needed).

## Acknowledgements
MS210 module brief and group collaboration.

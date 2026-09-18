# System Design Exercise

Our modelling team has built a new optimisation model that plans how a fleet of
power generators should run. Product wants our customers to run it on demand on
our web platform. Your job is to design the backend service around it.

## The model

You do not need to understand the optimisation itself, and we won't ask about
it. Treat the model as a black box with the following behaviour:

- A Python function, `solve(input) -> result`.
- It runs on one machine and uses all available CPU cores.
- It accepts input as JSON, typically 1–20 MB. Users submit via CSV.
- Its output is a schedule — which generators run, in which periods, at what
  output — and a total cost. Typically 5–50 MB.
- It typically takes 4–6 hours to solve. Sometimes 2, sometimes 8.

## Your task

Design the service:

- how a customer submits a run,
- how it executes,
- how they learn it's finished and get the result,
- and how it behaves when things go wrong.

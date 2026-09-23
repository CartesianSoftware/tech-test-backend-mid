# API Exercise: Electricity Prices

Build a small web service that serves electricity price information from a
CSV of historical data.

The `data/` directory holds one week of half-hourly wholesale electricity
prices for five Australian states. Your service should expose an HTTP API
that returns the mean price for a given state.

We expect this to take two to three hours. Please do not spend much longer
than that; we would rather see a focused, well-built slice than a sprawling
one.

## Requirements

Your service should:

- Load the provided data.
- Run a web server with at least one endpoint that takes a `state` and
  returns the mean price for that state.
- Include a `README.md` explaining how to set up, run and test it.

Anything not specified here is your call. Make a sensible decision and note
it in your README.

## Data

`data/prices.csv` has three columns:

| Column | Description |
| --- | --- |
| `state` | The state the price applies to. One of `NSW`, `QLD`, `SA`, `TAS`, `Vic`. |
| `price` | Wholesale price in AUD per MWh. Prices can be negative. |
| `timestamp` | Start of the 30-minute period the price applies to, e.g. `2025-06-24 00:30:00`. |

It covers 24 to 30 June 2025 inclusive: 336 rows per state, 1,680 in total.

## Tools

- Python or TypeScript is preferred, but use whatever language you are most
  productive in.
- Any language version that is not end of life.
- Any web framework and any supporting packages you think are appropriate.

## What we are looking for

- Clean, readable, maintainable code.
- A simple, well-structured application with a sensible API design.
- Sound handling of the data, including the edge cases you find in it.
- Tests, and a project layout that would be easy to hand to a teammate.

The dataset is small, but assume this service may one day need to handle much
larger datasets and higher request volumes. Design with that in mind where it
is cheap to do so, but do not over-engineer for it.

## Submission

Send your Endgame contact one of:

1. A link to a **private** Git repository (GitHub, GitLab, etc.) with your
   contact invited as a collaborator.
2. A zip of the repository, by email.

Please do not publish your solution publicly. See the
[licence](../LICENSE) for details.

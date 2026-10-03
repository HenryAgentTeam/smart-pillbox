# MVP and validation plan

## Goal

Demonstrate a reliable reminder and access-history loop that a user can interpret at a glance. Validate engineering behavior and usability separately from medical efficacy.

## MVP

One compartment, a local schedule, a lid sensor, a visible last-opening timestamp, an explicit confirmation action, configurable reminder outputs and durable event history. A caregiver view may initially use synthetic local events.

Defer automatic sleep detection, stock estimation, multi-compartment dispensing and medication-dependent physical locks. No real medication is needed for prototype testing.

## Milestones

1. Define the event schema and state machine.
2. Implement a deterministic simulator with synthetic fixtures.
3. Verify scheduling, opening, confirmation, overdue, reboot and invalid-clock cases.
4. Connect one sensor, display and reminder actuator.
5. Observe whether users distinguish opening from confirmed medication use.
6. Publish reproducible setup instructions, a demonstration and measured limitations.

## Baselines

Compare the same scripted tasks with a simple scheduled alarm and a last-opening timer. Measure trigger delay, missed/duplicate events, reboot retention, offline behavior, interpretation mistakes and time to find the last interaction.

Passing these checks does not prove that a reminder awakens a sleeping patient or reduces medication errors. Any such claim needs an appropriate independently governed evaluation.

## Open decisions

Board and SDK, sensor/display interfaces, safe actuator/power design, enclosure handling, caregiver delivery semantics and clinician-approved medication-specific requirements remain to be resolved. No hardware purchases or provider accounts are required to start the simulator.

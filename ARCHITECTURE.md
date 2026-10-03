# Architecture

The prototype separates deterministic medication-event tracking from optional presentation and synchronization.

## Components

- **Scheduler:** stores user-configured demonstration schedules and tracks clock validity.
- **Event store:** append-only events with IDs, device time, schedule version and sync state.
- **Sensor adapter:** debounces lid transitions; emits opening events without inferring ingestion.
- **Reminder controller:** controls configured vibration, sound and light channels.
- **State machine:** scheduled, reminder active, opened unconfirmed, self-confirmed, overdue and unknown.
- **Display:** one primary action and clear last-opening/confirmation labels; privacy-friendly defaults.
- **Sync adapter:** optional export of synthetic event status; offline state is visible. Real caregiver messaging is not implemented.

All core scheduling and logging should work offline. Reboots must preserve pending state and history. Repeated events and transport retries must not create duplicate confirmations. An invalid clock must be shown as unknown.

No LLM belongs on the dosing or state-transition path. Any future language feature may summarize recorded events but cannot invent medication actions.

## Planned layout

```text
simulator/
firmware/
tests/fixtures/synthetic/
docs/
```

These implementation directories will be introduced with the first code milestone.

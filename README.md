# Smart Pillbox

An open-source prototype exploring accessible medication reminders, visible access history, and caregiver awareness for people with narcolepsy.

**Status:** project definition and engineering plan. Firmware, hardware, and clinical effectiveness have not been validated.

## First prototype

Build one offline-capable loop:

1. Trigger a configured reminder.
2. Record a lid-opening event.
3. Distinguish an opening from explicit user confirmation.
4. Show an overdue or unknown state when confirmation is absent.
5. Retain the event history across reboot.

The device must never infer that opening the box proves medication was taken. It does not prescribe medication, generate dosing intervals, or recommend catch-up doses.

## Project documents

- [MVP and validation plan](docs/project-plan.md)
- [Architecture](ARCHITECTURE.md)
- [Contribution guidelines](CONTRIBUTING.md)

This is an independent implementation workspace inspired by the [OpenRD smart pillbox challenge](https://github.com/OpenRDHub/smart-pillbox). It is not the organizer's official repository. No upstream implementation or patient materials are included.

## Development

The first implementation milestone is a state-machine simulator using synthetic events. Hardware integration follows after its behavior is testable. No application is runnable yet.

## License

Original contributions in this repository are licensed under [Apache-2.0](LICENSE). This license does not establish or change the license of the separate OpenRD project or the terms of its contributor agreement.

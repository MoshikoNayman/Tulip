# Tulip Release Policy

By Moshiko Nayman.

This repository stores production releases and release downloads only.

## Release Designations

- `production release`: a versioned build that passed repository validation and was published to the Tulip production repository.
- `stable`: a stronger designation that may be used only after the required hardening checks are completed.

## Stable Criteria

A Tulip release may be called `stable` only when all of the following are true:

- lint passes for the shipped codebase
- typecheck passes for the shipped codebase
- production build passes for the shipped codebase
- the shipped desktop app is tested on a clean target machine
- platform-specific packaging checks pass for each platform being claimed as supported
- README, CHANGELOG, and LICENSE are present and accurate in the production repository
- the release is tagged using the required format `YY.QR Rx-Sx`

## Current Assessment

- `26.2R1-S1` qualifies as a production release
- `26.2R1-S1` should not yet be called `stable`
- a future `S2` or later hardening release may be designated stable if the criteria above are satisfied
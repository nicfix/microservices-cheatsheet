# Always Implement Snapshot Tests

## Status

Approved

## Context

When starting a new project, in a small team, one might have the temptation of skipping testing at all.

This is especially true in front-end code given the fast change of requirements and adjustments that are not-always-planned when dealing with User Interfaces.

Clarify the requirements, define again the scenarios and change the tests, make it red, make it green SHOULD be the way to do (TDD).

In some cases though we (developers) need to cut corners for a big number of reasons and often what gets cut is on the quality side (tests, continuous integration etc.).

In many projects, actually, there are no tests at all just because "they slow us down" or "we don't have deadlines that allow us to test the front-end".

On the other hand some-times, the project is in an exploration phase and the fast changes don't really allow the tests to be written.

In this context is crucial to have a technology that allows to write tests in a fast way, maybe auto-generated, given the last development status.

This technology would at least allow to write a basic set of tests that would serve the purpose to understand if something breaks in the rendered application.

## Decision

With the goal of implementing bare-minimum testing in ALL the scenarios.

Always Implement Snapshot Testing

## Consequences

Snapshot testing is cheap, is enough to write a test that invokes the component to:
* Create a snapshot of the rendered HTML at time t0
* Run against the previously generated snapshot at any change
* Clean up a no-more-valid snapshot and generate it again when the error detected by the test is an intentional change


Jest is probably the best option for React to implement snapshot testing. https://jestjs.io/docs/en/snapshot-testing
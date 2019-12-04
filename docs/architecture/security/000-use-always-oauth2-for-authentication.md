# Authenticate and Authorize using OAuth2

## Status

Proposed

## Context

Implementing authentication mechamisms in a microservices architecture brings several challenges.

The services might be exposed to different clients:
* Web
* Mobile
* Other Services
* 3rd Parties

Every client might require a different authentication schema. 
Implementing each one of them with a different technology could end up in an authentication hell that propagates through both the services and the clients involved.

OAuth2 defines several different flows that can be used in all the most frequent scenarios, check the following reference for more info https://auth0.com/docs/api-auth/which-oauth-flow-to-use.

## Decision

Use OAuth to implement any authentication flow.

## Consequences

OAuth2 might make both the architecture and the implementation of services more complex at the beginning.

In order to execute the authentication one might need an OAuth2 Provider implementation either hosted or As A Service (Firebase, OAuth0, etc.) or Open Source(https://oauth.net/code/).

Furthermore, the OAuth2 flows might intimidate at the beginning but the advantages are worth the hassle.

Several library implementations exist for the most used languages/platforms.

Please refer to this quide for an in-depth step-by-step overview of OAuth2.


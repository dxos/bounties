# Functions

## Problem

Applications need a way to synchronize external data with the state of application front-ends (ECHO) and vice versa.

Often, the location where that synchronization should run also requires external reachability (e.g. to receive webhook calls) and high availability (i.e. to avoid missing events).

There are few solutions that provide the combination of requirements:
- simple developer experience like Firebase Functions
- self-hosting ability
- open-source

The ECHO Agent is an example of a Function.

## Scenarios

A function which synchronizes email into ECHO.

A function that sends an email on request.

A function that react to changes in ECHO, does some processing, and then updates ECHO.

A function which silently replicates ECHO spaces for a user (agent).


# Pluggable Transports Specification

This repository tracks the ongoing development of the Pluggable Transports (PT) specification. It contains:

* Goals for the upcoming PT spec versions (this document)
* The PT proposal review status tracking proposals to change the PT spec
* Commonly proposed ideas which have not made it into the spec in the past

This document describes the goals for the PT spec on a per-release basis. This includes the next major
version and minor releases for the current major version. Each version of the spec will have smaller
features or minor changes independent of the larger goals, and not all goals will be reached in every
release.

For older versions of the spec, check the changelog in each spec document to see what changes were made in that version.

## Version Currently Under Development: 2.1

Expected finalization date: November 2018

### Goal: Additional Configuration Options

The PT 2.0 spec provides an Inter-Process Communication (IPC) protocol to configure a the PT as a proxy.
In 2.1 we will explore other options for configuration to see if other options might better meet the
needs of developers.

### Goal: Simplification

The PT IPC protocol is considered by some developers to be complex. In 2.1 we will consider options for
simplification. In particular, are there ways for the PT implementation to be more lenient, requiring
the developer to specify less without breaking compatibility with existing clients?

### Goal: Better Mobile Support

Support on mobile platforms such as Android and iOS have provided challenges to the way the PT 2.0 spec
allowed configuration of the PT implementation. In 2.1 we will explore how we can make things easier
for developers on mobile platforms.

### Goal: Additional API Flexibility

The PT 2.0 spec provides a Go API as an alternative to using the PT IPC protocol. The Go API is simple
and does not allow for advanced types of configuration. In 2.1 we will assess whether it is meeting the
needs of developers and what changes to the API could allow for better flexibility for practical use
cases for PTs in existing applications.

### Other Improvements

In PT 2.1, we will consider restructuring the PT specification to be more modular. Instead of one monolithic
document, we will be breaking it into smaller pieces. The goal of this process is to allow different
audiences of users to be able to read only the parts of interest to their needs, rather than contending
with all aspects of the specification at once.

### Backwards Compatibility

PT 2.1 will be backwards compatible with PT 2.0. This means that only the following changes are allowed:

- New capabilities can be added. For the Go API, this includes new packages, types, and functions. For the IPC layer this means new environment variables, command line flags, stdin/stdout lines, or perhaps a new means of communication not listed above.
- Constraints can be relaxed. For instance, required function parameters or environment variables can become optional.

The following changes are not allowed for this version:
- Removing capabilities. For the Go API, this includes removing or renaming packages, types, or functions. For the IPC layer this means removing or renaming environment variables or command line flags.
- Constraints cannot be further constraints. For instance, things which are optional cannot become required. New constraints can also not be added.

### Revision Process for PT 2.1

Proposal submission for PT 2.1 is now closed and the draft specification is being finalized for release. Proposals can still be submitted at any time, and they will be scheduled for review after the PT 2.1 specifiation has been finalized.

While implementations are not required to submit a proposal for consideration and discussion, they are required before a proposal can be included in a released draft of the specification.

## Previous Releases

* [PT 2.0]
* [PT 1.0]

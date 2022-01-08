# Pluggable Transports Specification



This repository tracks the ongoing development of the Pluggable Transports (PT) specification. It includes:

* releases - All versions of the PT specification
* proposals - Any proposals yet to be implemented

Inside the releases/latest folder are links to the latest versions of the specification. The most recent update is V2.2, 

The latest completed specification can be found in the releases folder, along with all numbered versions. The latest update was to the Dispatcher module, which is updated to V2.2. All other modules remain as their V2.1. Changes made in PT V2.2 are backwards-compatible with V2.1 and V2.0.

Keep an eye on the project Milestones for future plans, and Issues for the status of any proposed changes.

For older versions of the spec, check the changelog in each spec document to see what changes were made in that version.


### Modularity

Since PT 2.1, we have restructured the PT specification to be more modular. Instead of one monolithic document, it is broken into smaller pieces. The goal of this process is to allow different audiences of users to be able to read only the parts of interest to their needs, rather than contending with all aspects of the specification at once.

### Backwards Compatibility

PT 2.2 is compatible with PT 2.1 and 2.0. This means that only the following changes are allowed:

- New capabilities can be added. For the Go API, this includes new packages, types, and functions. For the IPC layer this means new environment variables, command line flags, stdin/stdout lines, or perhaps a new means of communication not listed above.
- Constraints can be relaxed. For instance, required function parameters or environment variables can become optional.

The following changes are not allowed for this version:
- Removing capabilities. For the Go API, this includes removing or renaming packages, types, or functions. For the IPC layer this means removing or renaming environment variables or command line flags.
- Constraints cannot be further constraints. For instance, things which are optional cannot become required. New constraints can also not be added.

### Revision Process for PT Spec

While implementations are not required to submit a proposal for consideration and discussion, they are required before a proposal can be included in a released draft of the specification.

## Proposals format

Draft proposals are prepared according to the preference of the group who's leading the drafting process. Once a proposal has been approvided by the Pluggable Transport Sterring Committee, it will be published in Markdown format in this repository. If past proposals are already published in other data formats, they will eventually be converted to Markdown. Previously existing files will not be removed from the repository to avoid breaking existing links.

## Previous Releases

* [PT 2.1]
* [PT 2.0]
* [PT 1.0]

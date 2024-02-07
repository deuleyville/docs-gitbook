# About

## Introduction

Welcome to the IonQ platform! You can use our API and the `qcloud` command-line interface to submit and retrieve jobs on our quantum hardware as well as our high-performance simulator.

Our API uses the [REST](https://en.wikipedia.org/wiki/Representational\_State\_Transfer) architectural style; this means we provide unsurprising, resource-oriented URLs and take advantage of built-in HTTP response codes, authentication, verbs, and other features. We allow cross-site requests from any domain, and return JSON responses.

If you prefer to not think about HTTP, use our [OpenAPI](https://www.openapis.org/) spec to generate bindings for your language of choice. Pre-generated bindings for Python and JavaScript are coming soon.

### Non-breaking changes

* Histogram example expanded to include scientific notation for a JSON numeric value.

### Migrating to v0.2

#### Breaking changes

* Calibrations endpoints has been deprecated in favor of Characterizations.

#### New features

* Ability to specifify target hardware generation on Job creation. e.g. `qpu.harmony` for targeting our 11-qubit system.
* Introduces Characterizations endpoints. Enables fetching current and historic characterizations for specific targets.
* Backends availability and other stats can now be fetched.

### Migrating to v0.1

#### Breaking changes

Prerelease version `v0.1` has one major breaking change from `v0`:

* Canceling jobs is now done via a PUT. This allows us to more naturally support job deletion.

#### New features

* Completely deleting one or more jobs is now possible
* Multiple jobs may be canceled simultaneously
* A list of jobs may be fetched simultaneously

### API status

API and quantum computer status is continuously reported at https://status.ionq.co/. Please subscribe for automated updates when we perform maintenance or experience an outage.

In addition, you may use the status endpoint to check the current status of our API.

### Authentication

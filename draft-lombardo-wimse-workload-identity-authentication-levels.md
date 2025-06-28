---
title: draft-lombardo-wimse-workload-identity-authentication-levels
category: info

docname: draft-lombardo-wimse-workload-identity-authentication-levels-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: ""
workgroup: WIMSE
keyword:
 - workload identity
 - authentication
 - microservices
venue:
 group: WIMSE
 type: Working Group
 mail: wimse@ietf.org
 arch: "https://mailarchive.ietf.org/arch/browse/wimse/"
 github: "identitymonk/draft-lombardo-wimse-workload-identity-authentication-levels"
 latest: "https://identitymonk.github.io/draft-lombardo-wimse-workload-identity-authentication-levels/draft-lombardo-wimse-workload-identity-authentication-levels.html"

author:
 -
    fullname: Jean-François Lombardo
    nickname: Jeff
    organization: AWS
    email: jeffsec@amazon.com
 -
   fullname: Marcel Levy
   organization: SPRL
   email: marcel@sprl.com
 -
   fullname: Dean Saxe
   organization: self
   email: dean@thesax.es

normative:

informative:
  NIST.SP.800-63:
    target: https://pages.nist.gov/800-63-3/
    title: NIST Special Publication 800-63 Digital Identity Guidelines
    date: June 2017
    author:
      -
        name: Paul A. Grassi
        role: editor
        organization: Applied Cybersecurity Division Information Technology Laboratory
      -
        name: Michael E. Garcia
        role: editor
        organization: Applied Cybersecurity Division Information Technology Laboratory
      -
        name: James L. Fenton
        role: editor
        organization: Altmode Networks Los Altos, Calif.


--- abstract

This document defines a framework for Machine Identity Assurance Levels (MIAL) and Machine Authentication Assurance Levels (MAAL) to establish consistent, verifiable trust in machine-to-machine communications.

--- middle

# Introduction

## Background

With the increasing complexity of distributed systems, containerization, and cloud-native architectures, machine and workload identity has become a critical security cornerstone. While for human identity standards guidance such as [NIST.SP.800-63]
provides comprehensive frameworks for human identity assurance and authentication, there is no equivalent standard for machine and workload identities.

This document defines a framework for Machine Identity Assurance Levels (MIAL) and Machine Authentication Assurance Levels (MAAL) to establish consistent, verifiable trust in machine-to-machine communications.

## Scope

This standard addresses:
- Machine identity proofing and verification requirements
- Machine authentication mechanisms and protocols
- Hardware-based security integration
- Supply chain validation requirements
- Runtime attestation and continuous verification
- Cross-environment identity federation
- Workload identity lifecycle management

# Conventions and Definitions

{::boilerplate bcp14-tagged}

The following terms are defined for use in this document:

- Machine Identity: A set of unique metadata and identifier associated with a hardware device, virtual machine, container, or workload.
- Workload: A discrete computing task or application running in a distributed environment.
- Attestation: The process of providing evidence about the state of a machine or workload.
- Identity Proofing: The process of verifying the claimed identity of a machine or workload.
- Authentication: The process of verifying the authenticity of a machine or workload identity.

# Framework Overview

The Machine Identity Assurance and Authentication Framework consists of two primary components:

## Machine Identity Assurance Levels (MIAL)

MIAL defines the degree of confidence in the claimed identity of a machine or workload. This includes:
- Supply chain validation
- Identity attestation
- Software integrity verification
- Configuration validation
- Deployment environment verification

## Machine Authentication Assurance Levels (MAAL)

MAAL defines the strength of an authentication nechanism used by workload to authenticate. This includes:

### Credential provider provenance

This represents the level of trust in the authenticator.

### Credential enrollment

This represents the requirements for the credential to exist.

### Credential containment

This represents the constraints on how and where the credential can be stored.

### Credential unlocking

This represents how the credential can be accessed for authentication purposes.

### Credential boundary

This represents the constraints on where the credential can be used.

### Credential reuse

This represents if and how one credential exist for more than one resource.

### Credential recovery

This represents the constraints on how the credential can be recoevered if somthing goes wrong.

### Credential governance

This represents the rules that govern the credential lifecycle.

### Level MAAL-0



# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.

--- back

# Acknowledgments
{:numbered="false"}


The authors wants to acknowledge the support and work of the following indivisuals: Ryan Hurst (Peculiar Ventures), Pamela Dingle (Microsoft).

The authors wants also to recognize the trail blazers and thought leaders that created the ecosystem without which this draft proposal would not be able to solve customer pain points and secure usage of digital services, especially without being limited to: Vittorio Bertocci†, Brian Campbell (Ping Identity), Justin Richer (MongoDB), Aaron Parecki (Okta), Pieter Kasselman (SPRL), Dr Mike Jones (Self-Issued Consulting, LLC), Dr Daniel Fett (Authlete).

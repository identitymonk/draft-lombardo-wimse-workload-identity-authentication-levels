# Workload Identity Authentication Levels

## Level 0: No Authentication

### Description:
- No authentication mechanisms are in place.

### Characteristics:
- Machines and workloads operate without any form of authentication.
- No assurance of identity or integrity of dependent services.
- Highly vulnerable to unauthorized access and attacks.

### Examples:
No access control or reliance on IP addresses, combined with allow lists and block lists for access control.

## Level 1: Deploy Time Shared-Secret Based Authentication

### Description:
Manual deploy time of simple passwords, shared secrets and API keys without lifecycle management

### Characteristics:
- Use of simple shared secrets (e.g., passwords, API keys) deployed manually or at deploy time.
- No unique identification of workloads.
- Minimal automation in credential distribution typically without regular credential rotation.
- Lack of instrumentation on credential lifecycle and governance reporting.
- Highly vulnerable to key compromise and lateral movement of attackers.

### Examples:
Deploy-time shared secrets.

## Level 2: Deploy-Time Credential Based Authentication

### Description:
Static asymmetric key-based authentication and symmetric credential management systems that are deployed during setup.

### Characteristics:
- Use of static credentials (e.g., long-lived certificates).
- Minimal automation in credential distribution.
- Basic security policies and procedures in place.
- No reliable credential lifecycle management
- Often no governing authority for credential issuance, leading to issues such as password sprawl and difficulty in governance.

### Examples:
Kerberos key tabs, long-lived tokens.

## Level 3: Automated Authentication with Static Credentials

### Description:
Automated authentication using static credentials and improved logging.

### Characteristics:
- Use of static credentials (e.g., long-lived certificates, tokens).
- Improved logging and monitoring capabilities.
- Automated processes for credential distribution.
- Basic security policies and procedures in place.
- Access controls tied to the credential rather than the subject of the credential due to the lack of an issuer/governing authority.

### Examples:
Automated API key distribution, long-lived certificates managed through automation tools.

## Level 4: Dynamic Authentication with Renewable Credentials

### Description:
Dynamic authentication using renewable credentials with moderate automation.

### Characteristics:
- Use of renewable credentials (e.g., short-lived certificates, tokens).
- Automated credential issuance and renewal processes.
- Enhanced logging and monitoring with anomaly detection.
- Regular auditing and compliance checks.

### Examples:
Short-lived tokens issued and renewed automatically, dynamic certificates.

## Level 5: Zero-Trust Principles with Context-Aware Authentication

### Description:
Implementation of zero-trust principles with context-aware authentication.

### Characteristics:
- Use of context-aware, short-lived credentials (e.g., ephemeral certificates, workload identities).
- Continuous authentication and authorization checks based on context (e.g., behavior, location).
- Advanced logging, monitoring, and real-time threat detection.
- Integration with identity management and access control systems.

### Examples:
Ephemeral certificates, workload identities validated against behavioral baselines.

## Level 6: Full Zero-Trust Implementation with End-to-End Security

### Description:
- Comprehensive zero-trust security with end-to-end protections.

### Characteristics:
- End-to-end encryption and mutual authentication for all communications.
- Full implementation of dynamic, context-aware authentication and authorization.
- Automated security policy enforcement and compliance monitoring.
- Robust threat intelligence integration and proactive threat mitigation.
- Continuous improvement and adaptation to emerging threats and vulnerabilities.

### Examples:
- Full zero-trust network architecture, real-time threat intelligence integration.
- Naming and Attestation: Ability to identify the combination of machine and workload, with attestation providing assurance of the state of the environment.

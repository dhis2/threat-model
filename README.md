# DHIS2 Threat Model

## Scope

- DHIS2 server application (backend)
- DHIS2 mobile application

## Principals

### DHIS2 User

- Can sign up for an account
- Can see the list of other DHIS2 users
- Can read or write according to the access control permissions

### DHIS2 Administrator

- Can read or write DHIS2 data
- Can read or write DHIS2 metadata
- Can change system-wide settings
- Can install DHIS2 web applications
- Can configure integrations with other systems
- Can manage users, groups, and roles

### DHIS2 Server Administrator

- Can access server console and DHIS2 database with administrative permissions
- Can configure database backup

## Adversaries

- An external threat actor without access to DHIS2 (anonymous hacker)
- A legitimate DHIS2 user with malicious intentions
- A legitimate DHIS2 Server Administrator with malicious intentions

We are treating malicious intentions as an external threat actor with access to the compromised device or credentials of a legitimate DHIS2 user.

## Trust Assumptions

- Hardware or cloud environment is trusted, so DHIS2 doesn't implement or expect any security controls at this level
- DHIS2 Server Administrator has full access to the DHIS2 database, database encryption key, and secrets stored in the DHIS2 database

## Security Objectives

- Authenticate a legitimate user
- Allow password reset for a legitimate user

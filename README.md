# DHIS2 Threat Model

## Scope

- DHIS2 server application (backend)
- DHIS2 mobile application

## Principals

### DHIS2 User

- Can sign up for a DHIS2 account
- Can change the settings of the account
- Can change or recover password
- Can see the list of other DHIS2 users
- Can send messages to other DHIS2 users
- Can read or write DHIS2 data
- Can read, write, and sync the offline copy of DHIS2 data in the mobile application

### DHIS2 Administrator

- Can read or write DHIS2 data
- Can read or write DHIS2 metadata
- Can impersonate other users
- Can change system-wide settings
- Can install DHIS2 web applications
- Can configure integrations with other systems
- Can manage users, groups, and roles

## Adversaries

- An external threat actor without access to DHIS2 (hacker)
- A legitimate DHIS2 User with malicious intentions
- A legitimate DHIS2 Administrator with malicious intentions

We treat the malicious intentions of a legitimate user as actions of an external threat actor with access to the compromised device or credentials of a legitimate DHIS2 user.

## Trust Assumptions

- DHIS2 server application build files, web applications from the App Hub, and mobile application packages are trusted
- Hardware or cloud environment for the deployment is trusted, so DHIS2 doesn't implement or expect any security controls at this level
- DHIS2 server administrator has full access to the DHIS2 database, database encryption key, and secrets stored in the DHIS2 database

## Security Invariants

- An unauthenticated party can't confirm presence of a specific DHIS2 user account
- Any sensitive operation requires re-authentication
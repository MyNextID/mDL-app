# mDL App Validate Authorization request Requirements

- **Version of this document**: 1.0.0
- **Last Updated**: September 22, 2023
- **Conformant with Specification**: ISO/IEC 18013-5, ISO/IEC 18013-7, Annex B


## Requirement ID: Validate-AR-REQ-001
### GET Response is valid JWS
- **Mandatory**: Yes
- **Verification Step**: Verify that body of a HTTP GET to "request_uri" is a JWS and parse it.

## Requirement ID: Validate-AR-REQ-002
### Client metadata
- **Mandatory**: Yes
- **Verification Step**: Verify that JWS payload contains "client_metadata".

## Requirement ID: Validate-AR-REQ-003
### Reader public key
- **Mandatory**: Yes
- **Verification Step**: Verify that "client_metadata" contains "jwks", which is an array that contains valid JWK keys.

## Requirement ID: Validate-AR-REQ-004
### Client ID
- **Mandatory**: Yes
- **Verification Step**: Verify that request contains parameter "client_id".

## Requirement ID: Validate-AR-REQ-005
### Response URI
- **Mandatory**: Yes
- **Verification Step**: Verify that request contains parameter "response_uri".

## Requirement ID: Validate-AR-REQ-006
### Nonce
- **Mandatory**: Yes
- **Verification Step**: Verify that request contains parameter "nonce".

## Requirement ID: Validate-AR-REQ-007
### Presentation definition
- **Mandatory**: Yes
- **Verification Step**: Verify that request contains parameters "presentation_definition" > "input_descriptors" > "contraints" > "fields".


---
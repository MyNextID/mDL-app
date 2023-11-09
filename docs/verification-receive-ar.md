# mDL App Receive Authorization request Verification Requirements

- **Version of this document**: 1.0.0
- **Last Updated**: September 22, 2023
- **Conformant with Specification**: ISO/IEC 18013-5, ISO/IEC 18013-7, Annex B


## Requirement ID: Receive-AR-REQ-001
### Parameter - request_url
- **Mandatory**: Yes
- **Verification Step**: Verify that mdl Reader provided url contains query parameter "request_url".

## Requirement ID: Receive-AR-REQ-002
### Parameter - request_url is a valid URL
- **Mandatory**: Yes
- **Verification Step**: Verify that value of "request_url" is a valid URL.

## Requirement ID: Receive-AR-REQ-003
### Parameter - request_uri
- **Mandatory**: Yes
- **Verification Step**: Verify that URL in "request_url" parameter contains parameter "request_uri".

## Requirement ID: Receive-AR-REQ-004
### Parameter - request_uri is a valid URL
- **Mandatory**: Yes
- **Verification Step**: Verify that value of "request_uri" is a valid URL.

## Requirement ID: Receive-AR-REQ-005
### Parameter - request_uri 
- **Mandatory**: No
- **Verification Step**: Check if URL in "request_uri" parameter contains parameter "tx_id".


---
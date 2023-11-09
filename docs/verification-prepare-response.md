# mDL App Prepare Authorization response Definitions

- **Version of this document**: 1.0.0
- **Last Updated**: September 22, 2023
- **Conformant with Specification**: ISO/IEC 18013-5, ISO/IEC 18013-7, Annex B


## Definition ID: Prepare-response-DEF-001
### Apu
- **Mandatory**: Yes
- **Step**: Defines apu value (agreement PartyUInfo - value for key agreement algorithms such as "ECDH-ES"). Value is string.

## Definition ID: Prepare-response-DEF-002
### APV
- **Mandatory**: Yes
- **Step**: Defines apv value (agreement PartyVInfo - value for key agreement algorithms such as "ECDH-ES"). Value is string.

## Definition ID: Prepare-response-DEF-003
### Device nameSpaces
- **Mandatory**: Yes
- **Step**: Defines device nameSpaces as an empty map {} and CBOR encodes it.

## Definition ID: Prepare-response-DEF-004
### Algorithm
- **Mandatory**: Yes
- **Step**: Defines signing algorithm cose.AlgorithmES256 and sets it as a protected header.

## Definition ID: Prepare-response-DEF-005
### Session transcript
- **Mandatory**: Yes
- **Step**: Defines Session transcript as an object containing base64URL encoded apu and client_id, response_uri and nonce parameters from authorization request.

## Definition ID: Prepare-response-DEF-006
### Device authentication
- **Mandatory**: Yes
- **Step**: Defines Device authentication as an object containing string "DeviceAuthentication", session transcript, string "org.iso.18013.5.1.mDL" and cbor encoded device nameSpaces.
This object is signed with mDL App private key and the signature is used for mdoc authentication by mDL Reader.

## Definition ID: Prepare-response-DEF-007
### Issuer nameSpaces
- **Mandatory**: Yes
- **Step**: Prepares Issuer nameSpaces based on "fields" received in authorization request's "presentation_definition". 

## Definition ID: Prepare-response-DEF-008
### Digest ID
- **Mandatory**: Yes
- **Step**: Defines random, unique integer, that is lower than 2^31 for every "field".

## Definition ID: Prepare-response-DEF-009
### Element value
- **Mandatory**: Yes
- **Step**: Retrieves requested element value for every "field".

## Definition ID: Prepare-response-DEF-010
### Random
- **Mandatory**: Yes
- **Step**: Defines Random as a random hex string of length 16.

## Definition ID: Prepare-response-DEF-011
### NameSpace
- **Mandatory**: Yes
- **Step**: Each nameSpace contains an array of data fields - objects with Digest ID, ELement Identifier (from "fields" in "presentation_definition"), Element value and Random.

## Definition ID: Prepare-response-DEF-012
### Value Digests
- **Mandatory**: Yes
- **Step**: Defines Value digests as a pair of corresponding Digest ID and hash of whole Data field.

## Definition ID: Prepare-response-DEF-013
### Version
- **Mandatory**: Yes
- **Step**: Defines version as a string "1.0".

## Definition ID: Prepare-response-DEF-014
### Digest Algorithm
- **Mandatory**: Yes
- **Step**: Defines Digest Algorithm as a string "SHA-256".

## Definition ID: Prepare-response-DEF-015
### DocType
- **Mandatory**: Yes
- **Step**: Defines DocType as a string "org.iso.18013.5.1.mDL".

## Definition ID: Prepare-response-DEF-016
### ValidityInfo
- **Mandatory**: Yes
- **Step**: Defines ValidityInfo as an object of "signed", "validFrom" and "validUntil" timestamps, formatted as "2006-01-02T15:04:05Z".

## Definition ID: Prepare-response-DEF-017
### MSO
- **Mandatory**: Yes
- **Step**: Defines MSO (MObileSecurityObject) as an object of version, digest algorithm, value digests, deviceKeyInfo, docType and validityInfo.








---
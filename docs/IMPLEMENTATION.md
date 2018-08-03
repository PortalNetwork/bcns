# Implementation

## BCNS Spec

The internet HTTP protocol is using the URL below:

```
<protocol>://<subdomain>.<domain>.<top-level domain>/<path>
```

Example:
```
https://www.portal.bch/path
```

#### Spec
- http: The BCNS and protocol will be passed separately when the service requests.
- www.portal.bch: The content of the BCNS is used when user requests to the browser.
- path: The path is not processed at the DNS level, the same as BCNS, if there is a path, it is handled by other way or method.

## Resolving Names
Resolving names in BCNS is a three step process:
1. Normalise and hash the name you want to resolve.
2. Query the BCNS registry for the address of the resolver responsible for the name.
3. Query the resolver for the resource you want to look up.

## Updating BCNS Records
Your application may wish to provide users with a means of updating names they own to point to resources your application provides or manages. Doing so follows a similar process to [Resolving Names](#resolving-names):

- Normalise and hash the name you want to resolve.
- Query the BCNS registry for the address of the resolver responsible for the name.
- Call the appropriate update method on the resolver.

In order to preserve the hierarchal nature of names, namehash is defined recursively, making it possible to derive the hash of a subdomain from the namehash of the parent domain and the name or hash of the subdomain label.

### Terminology
- domain - the complete, human-readable form of a name; eg, `wallet.portal.bch`.
- label - a single component of a domain; eg, `portal`, `wallet`, or `bch`. A label may not contain a period ('.').
- label hash - the output of the keccak-256 function applied to a label.
- node - the output of the namehash function, used to uniquely identify a name in BCNS.

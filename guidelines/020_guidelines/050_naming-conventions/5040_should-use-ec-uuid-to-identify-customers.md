---
type: SHOULD NOT
id: R100078
---

# use ec-uuid (or uuid) to identify customers

The ec-uuid (sometimes just called UUID) is the recommended way to identify logged in customers. It is not easily enumerated (as the account number) and is stable between sessions and devices.

Also, for endpoints that work with user-based scopes (i.e. retrieving a customers shipment overview) it is included in the JWTs sub (or subject) claim and thus signed by the authentication server.

An example can be found in the [OAuth2 section](guidelines/020_guidelines/020_security/1000_oauth2.md). For the subject claim to be filled the client needs to implement the [authorization code grant flow](guidelines/020_guidelines/020_security/1020_must-use-authorization-grant.md) (in which the user gives his permission).
# Privanta bootstrap recovery mirror

This repository contains only the public, detached-signature bootstrap
artifacts used by Privanta clients when the primary configuration domains are
unavailable.

Clients trust the offline Ed25519 root key embedded in the application. They
do not trust this repository, its Git history, GitHub TLS, or the workflow as a
configuration authority. Invalid, expired, equivocal, or rolled-back content
is rejected locally.

The mirror workflow accepts an update only when the primary and recovery
origins are byte-identical, the detached root signature verifies, the revision
does not decrease, and the manifest retains at least 14 days of validity.

Public endpoints:

* `https://raw.githubusercontent.com/Privanta-vpn/privanta-bootstrap/main/v1/bootstrap`
* `https://raw.githubusercontent.com/Privanta-vpn/privanta-bootstrap/main/v1/bootstrap.sig`

No credentials, device identifiers, customer data, traffic data, or private
keys belong in this repository.

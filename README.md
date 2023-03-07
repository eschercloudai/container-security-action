# Container Security Scan :lock:

This action exists to combine a set of common tasks for running [Grype](https://github.com/anchore/grype) and [Syft](https://github.com/anchore/syft).

Generally speaking when scanning a container you should generate an SBOM, scan the SBOM and then scan the resulting image.
When the container is ready to be pushed, it will do so and then sign the container using [Sigstore Cosign](https://github.com/sigstore/cosign).
This will require additional parameters passing in such as a key.

Whilst nothing can catch everything, this gives a wide view of what is going on within an image.

## TODO:
* Generate easy to read report for the scans to allow easy browsing of the scan results.
* Support dynamic key generation for Cosign.
* Support OIDC cosign signing.
* Support adding to Rekor (currently does not do this by default to prevent any private images being added when the user may not want this to happen)

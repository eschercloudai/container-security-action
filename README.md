# Container Security Scan :lock:

This action exists to combine a set of common tasks for running [Grype](https://github.com/anchore/grype) and [Syft](https://github.com/anchore/syft).

Generally speaking when scanning a container you should generate an SBOM, scan the SBOM and then scan the resulting image.
Whilst nothing can catch everything, this gives a wide view of what is going on within an image.

## TODO:
* Add [Sigstore](https://github.com/sigstore/cosign) image signing into the mix
* Generate easy to read report for the scans to allow easy browsing of the scan results. 

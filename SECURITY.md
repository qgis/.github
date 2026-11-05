# Reporting security issues

## QGIS core vulnerabilities

Please report security issues and vulnerabilities at https://github.com/qgis/.github/security/advisories

## Websites and associated projects

Please report security issues and vulnerabilities at https://github.com/qgis/.github/security/advisories

## Reporting a vulnerability in our installers

QGIS.org maintains:

- Windows packages, through the OSGeo4W project
- macOS installers
- Debian/Ubuntu packages

For Windows and macOS, the installers bundle many dependencies, so scanners will often detect CVEs.
Before reporting, please:

1. Check that you are using the latest security release (published monthly) and a supported major version of QGIS. The roadmap is available at https://qgis.org/resources/roadmap/#qgis-prereleases
2. Check whether the upstream projects have already been patched, before asking us for an upgrade.
3. Check that your scanner is not raising a false positive.

> For instance, the PostgreSQL server is **not** shipped in our installers, but QGIS does ship the PostgreSQL **client** libraries. Most CVE catalogs do not distinguish between client and server components, which results in unnecessary noise.

Finally, many antivirus programs tend to raise false positives for the numerous executable files shipped with GRASS, which follow a naming convention such as `r.sun.exe`. Heuristic (Bayesian) detection tools often classify these files as dangerous. Please take the time to whitelist them yourself, as we cannot do it for you.

## Community installers

Many packages are maintained by the community, such as Flatpak, Conda, and Snap. In this case, please contact the maintainers of the relevant project.

Others depend on the distribution you use, such as apt or pacman. In this case, dependencies are handled as part of your regular system upgrades.

## Mailing list

The security@qgis.org mailing list can be used to discuss topics broader than vulnerabilities.

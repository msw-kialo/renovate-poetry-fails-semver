# Renovate reproduction repo

The Poetry manage appears to not upgrade python packages with four components (mostly `types-*` package).

Add add `types-` package to a poetry project:

`poetry add types-X`

It will add a contraints like `^1.2.3.0` (usually 1.2.3 is the original upstream version; and 0 is the
revisition of the typing package).

Renovate does not detect this updates. It detects however `>= 1.2.3.0` etc.

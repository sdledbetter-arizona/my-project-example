# SailPoint Identity Governance Ontology Example

A small example project built with the [SailPoint Identity Governance Ontology](https://github.com/sdledbetter-arizona/my-project), which it installs as the package `@oml/my-project`.

## Setup

1. Make sure the package is available in your local registry: start the registry from [`verdaccio`](https://github.com/modelware/verdaccio) and publish SailPoint Identity Governance Ontology to it, as described in their READMEs.
2. Install the method into this repository:
   ```bash
   oml install -r http://localhost:4873
   ```
   It is installed into `deps/@oml/my-project/`.

## Use

Open this repository in OML Code. The model's Sierra imports resolve to the installed package, and the notebooks in `src/md/Identity Governance` use SailPoint Identity Governance Ontology's templates.

From the command line (requires signing in to OML):

```bash
oml start
oml lint
oml codegen -c conops
oml codegen -c device
oml stop
```

The generator come with the SailPoint Identity Governance Ontology package: `sm1` writes `build/docs/source-accounts-count.md`.

## Upgrading SailPoint Identity Governance Ontology

A plain `oml install` keeps the installed version. To move to a newer one, name it:

```bash
oml install @oml/my-project@^0.1.1 -r http://localhost:4873
```
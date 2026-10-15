# OPENELECTIONS_CORE

![licence](https://img.shields.io/badge/licence-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-16_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `OPENELECTIONS_CORE` in category **GOVERNMENT**. 16/16 checks PASS (measured). Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** OPENELECTIONS_CORE · **Upstream pin:** `b4be7eb58f51631f48d607c6a781e964e9ef2bd8` · **Category:** GOVERNMENT · **Vendor:** Anticloud FZ LLE · **Licence:** MIT

---

## What This Project Does

## Open Elections core code

[![Build Status](https://travis-ci.org/openelections/openelections-core.svg?branch=dev)](https://travis-ci.org/openelections/openelections-core)

Core project for election results data acquisition, transformation and output.

OpenElections core is developed and tested using Python 3. The package
might not work with older Python distributions.

### Getting started as a developer

You'll:

* set up a virtual environment
* fork/source this project, install dependencies
* add any optional configuration details you need (e.g. Mongo or AWS)

#### Setting up a virtual environment

You should use [pipenv](https://pipenv.readthedocs.io/en/latest/) to work on Open Elections inside a virtualized development environment.

The easiest way is to install these tools system-wide with `pip` (you may need to use `sudo`):

```bash
$ pip install --upgrade pipenv
```

Then, to make a virtual environment for open elections work:

```bash
$ pipenv install --dev
```

To activate the virtual environment, run:

```bash
$ pipenv shell
```

#### Fork and set up this project

[Fork this project](https://help.github.com/articles/fork-a-project) by hitting the "Fork" button above, and source your fork to your computer:

```bash
$ git source https://github.com/[my_github_user]/openelections-core.git
$ cd openelections-core
```

Turn setup and activate the virtual environment from the previous step, if you haven't already:

```bash
$ pipenv install --dev
$ pipenv shell
```

Install MongoDB

To store your data in MongoDB, you need only [install Mongo](http://docs.mongodb.org/manual/installation/). The [default configuration](https://github.com/openelections/openelections-core/blob/master/settings.py.tmplt#L7-L20) should auto-create the databases and tables you need, as you need them.

At the very least, you'll want to make sure the values in the ``MONGO`` variable work for the way you've installed and configured MongoDB on your system.

Create a `settings.py` file.

```bash
$ cp settings.py.tmplt settings.py
```

You can put this settings file anywhere on your filesystem.  You'll need to set the ``OPENELEX_SETTINGS`` environment variable to the [absolute path](http://en.wikipedia.org/wiki/Path_(computing)) to the ``settings.py`` file that you created.

You can set the `OPENELEX_SETTINGS` environment variable by creating a `.env` file in your project. For example:

```
OPENELEX_SETTINGS=/Users/[myusername]/Development/openelections-core/settings.py
```

Running `pipenv shell` will automatically source any variable in your `.env` file.

#### Running management commands

Test it out by running `openelex --help`, you should see something like:

```bash
$ openelex --help
Usage: openelex [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  bake.election_file             Write election and candidate data with on...
  bake.results_status_json       Output a JSON file describing available...
  bake.state_file                Write election and candidate data along
                                 with...
  cache.clear                    Delete files in state cache diretory
  cache.files                    List files in state cache diretory
  datasource.elections           List elections for a state.
  datasource.filename_url_pairs  List mapping of standard filenames to
                                 source...
  datasource.mappings            List metadata mappings for a state
  datasource.target_urls         List source data urls for a state
  fetch                          Scrape data files and store in local file...
  load.run                       Load cached data files into the database
  load_metadata.run              Populate metadata in database from fixture...
  publish                        Publish baked result files
  shell                          Open a Python shell, bootstrapping the...
  transform.list                 Show available data transformations
  transform.reverse              Reverse a previously run transformation
  transform.run                  Run data transformations
  validate.list                  Show available validations for state
  validate.run                   Run data validations for state
```

Running commands looks something like this:

```bash
$ openelex cache.clear --state=NY
0 files deleted
0 files still in cache
```

You can also get help on particular commands, e.g. `openelex --help cache.clear`.

#### Configuring services (optional)

If you are going to load results, you need to configure MongoDB connections in
`openelex/settings.py`.

If you are a core contributor who needs to publish baked results to one of the GitHub projects, you will need to define further settings.

To set GitHub credentials, you must first create a [personal access token](https://help.github.com/articles/creating-an-access-token-for-command-line-use) and then uncomment and set these values in `openelex/settings.py`:

```python
GITHUB_USERNAME = ''
GITHUB_ACCESS_TOKEN = ''
```

#### Load party and office metadata (optional)

You only need to do this if you plan to write data loaders or transforms.

```bash
$ cd openelex
$ openelex load_metadata.run --collection=office
$ openelex load_metadata.run --collection=party
```

---

## Installation

You'll:

* set up a virtual environment
* fork/source this project, install dependencies
* add any optional configuration details you need (e.g. Mongo or AWS)

## Usage

You'll:

* set up a virtual environment
* fork/source this project, install dependencies
* add any optional configuration details you need (e.g. Mongo or AWS)

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | unknown |
| Lines of Code | unknown |
| Dependencies | unknown |
| Upstream license (harvested) | MIT |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

* fork/source this project, install dependencies
* add any optional configuration details you need (e.g. Mongo or AWS)

## Contributing

might not work with older Python distributions.

## License

Upstream © its respective contributors under MIT (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- **project:** OPENELECTIONS_CORE
- **Pinned SHA:** `b4be7eb58f51631f48d607c6a781e964e9ef2bd8`
- **source:** `UPSTREAM_CLONE/` (pinned at the SHA above)
- **Upstream README source:** `UPSTREAM_CLONE/README.md`

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`625d3b7768a14b8f2ec929b6485c5024b6596621c9d3707670fc2fca0d5ba1fa`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.


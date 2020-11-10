# Darwin Core

Darwin Core is a standard maintained by the [Darwin Core Maintenance Interest Group](https://www.tdwg.org/standards/dwc/#maintenance%20group). It includes a glossary of terms (in other contexts these might be called properties, elements, fields, columns, attributes, or concepts) intended to **facilitate the sharing of information about biological diversity** by providing identifiers, labels, and definitions. Darwin Core is primarily based on taxa, their occurrence in nature as documented by observations, specimens, samples, and related information.

## Getting started

[Darwin Core quick reference guide](https://dwc.tdwg.org/terms/)

Documents:

* [List of terms document](https://dwc.tdwg.org/list/): Comprehensive metadata for current and obsolete terms in human readable form 
* [Complete term history table](vocabulary/term_versions.csv): A CSV file with the full version history of Darwin Core terms
* [Distribution documents](dist/): Simple CSV files to start using Darwin Core
* [Website documents](docs/): Markdown files that form the source for the [Darwin Core website](https://dwc.tdwg.org/)

Community:

* [How to contribute](.github/CONTRIBUTING.md): a guide on how to contribute to Darwin Core
* [Darwin Core Q&A](https://github.com/tdwg/dwc-qa): an open forum on the use of Darwin Core

## Repo structure

The repository structure is described below. Files/directories indicated with `GENERATED` should not be edited manually.

```
├── .github
│   ├── ISSUE_TEMPLATE        : Directory of issue templates generated by GitHub
│   ├── CONTRIBUTING.md       : Guide on how to contribute, create issues, etc.
│
├── build
│   ├── doe-cv-build : Directory of build scripts for the degreeOfEstablishment controlled vocabulary
│   ├── em-cv-build  : Directory of build scripts for the establishmentMeans controlled vocabulary
│   ├── pw-cv-build  : Directory of build scripts for the pathway controlled vocabulary
│   ├── README.md                 : Workflow for generating a new version of the vocabulary
│   ├── build-termlist.ipynb      : Juyter notebook to construct the term list
│   ├── build-temlist.py          : Script to build Markdown pages that provide term metadata for complex vocabularies
│   ├── build.py                  : Build script to generate distribution files from the normative document
│   ├── generate_term_versions.py : Script to build the terms_versions.csv file
│   ├── qrg-list.csv              : List of the term IRIs in the order that they are to appear in the Quick Reference Guide
│   ├── requirements.txt          : List of libraries required by the build scripts
│   ├── termlist-footer.md        : Footer to append to the generated term list document
│   ├── termlist-header.md        : Header to prepend to the generated term list document
│   ├── terms.tmpl                : A Jinja2 template to format the Quick Reference Guide
│   └── workflow_diagram.png      : Figure used in README.md to show how to create a new version of the standard
├── dist                          : GENERATED Distribution files generated by build.py
│   ├── simple_dwc_horizontal.csv : GENERATED CSV file with Simple Darwin Core terms as a row
│   └── simple_dwc_vertical.csv   : GENERATED CSV file with Simple Darwin Core terms as a column
│
├── docs
│   ├── doe               : Degree of Establishment Controlled Vocabulary List of Terms
│   ├── em                : Establishment Means Controlled Vocabulary List of Terms
│   ├── list              : Darwin Core List of Terms documents
│   ├── namespace         : Darwin Core namespace policy
│   ├── pw                : Pathway Controlled Vocabulary List of Terms
│   ├── rdf               : Darwin Core RDF Guide
│   ├── simple            : Simple Darwin Core Guide
│   ├── terms
│   │   └── index.md      : Content for Quick Reference Guide generation using Jekyll
│   │
│   ├── text              : Darwin Core Text Guide (Darwin Core Archive specification)
│   ├── xml               : Darwin Core XML Guide
│   ├── _config.yml       : Jekyll site configuration for Quick Reference Guide
│   ├── CNAME             : Canonical Name record for dwc.tdwg.org
│   └── index.md          : Header for Darwin Core web site generation using Jekyll
│
├── vocabulary
│   └── term_versions.csv : Darwin Core term versions, contains the complete history of the terms
│
├── .gitignore            : Files and directories to be ignored by git
├── LICENSE               : Repository license
└── README.md             : Description of this repository
```

## Contributors

[List of contributors](https://github.com/tdwg/dwc/contributors)

## License

[Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/)

## Recommended citation

For Darwin Core in general, consider the peer-reviewed article on Darwin Core:

> Wieczorek J, Bloom D, Guralnick R, Blum S, Döring M, et al. (2012) Darwin Core: An Evolving Community-Developed Biodiversity Data Standard. PLoS ONE 7(1): e29715. https://doi.org/10.1371/journal.pone.0029715

For this repository:

> Darwin Core Maintenance Interest Group, Biodiversity Information Standards (TDWG) (2014). Darwin Core. Zenodo. https://doi.org/10.5281/zenodo.592792

The citation above represents all versions of the repository. Specific [versions/releases](https://github.com/tdwg/dwc/releases) from 2011 onwards are also deposited on Zenodo.

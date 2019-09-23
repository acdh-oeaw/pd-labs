# PARTHENOS Discovery Labs

Various scripts and results for exploring and curating the data of the [PARTHENOS Project](http://www.parthenos-project.eu/).

[PARTHENOS Discovery](https://parthenos.acdh.oeaw.ac.at/) is an application that gives access to the metadata records contributed by the partners of the PARTHENOS project, research infrastructures and initiatives in the broad domain of humanities and cultural heritage.
These records are being regularly harvested   converted into a common semantic model, the PARTHENOS Entities Model (PEM) and ingested into a triple store. PARTHENOS Discovery allows to navigate, explore and search this data.

Due to the heterogeneity and idiosyncracies of the contributed datasets as well as due to the complex mapping process, the aggregated dataset exhibits a number of [issues regarding the data quality](DataQuality.md)

Nevertheless, we believe the resulting combined dataset is an exciting resource, allowing a synoptic view over a huge dataspace. It represents a solid basis for further curation and harmonisation efforts.

This repository is meant to offer means for advanced querying and evaluation of the dataset as well as to keep track of curation issues.

## Data notebooks

Under (scripts/notebooks)[scripts/notebooks] you can find sample python notebook(s) demonstrating programmatic querying of the SPARQL endpoint using python programming language. These data notebooks are ideal means for manifold data science tasks especially for working in a collaborative distributed environment. They allow to share code and thus reproduce results in a trivial manner.
You do need a dedicated [jupyter](https://jupyter.org/) environment, however next to simple options to setup one locally, there are more and more offers providing appropriate environment as a service.

Information about local installation options:
* [Anaconda](https://www.anaconda.com/distribution/) - scientific Python distribution, includes Jupyter out of the box
* [Jupyter Docker Stack](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)

Some services offering jupyter:
* https://colab.research.google.com/notebooks/welcome.ipynb
* https://marketplace.eosc-portal.eu/services/egi-notebooks
* https://jupyter.org/try

There is an initial sample notebook [Querying PD.ipynb](scripts/ipynb/Querying PD.ipynb) with multiple examples of queries run against the SPARQL endpoint.
This is based on previous work by Paul Houle: [gastrodon](https://github.com/paulhoule/gastrodon/blob/master/notebooks/remote/Querying%20DBpedia.ipynb) and is using [Pandas](https://pandas.pydata.org/pandas-docs/stable/) - a Python data analysis library; sometimes called "Excel for Python" - for holding the results of the query and further processing it in a ["DataFrame"](https://pandas.pydata.org/pandas-docs/stable/reference/frame.html#).


## Curation

We are aware that the PARTHENOS Discovery dataset is not "perfect". We are continuously working on improving the dataset. This repository is also meant to communicate the status and known quality issues of the dataset. At the same time, it serves as a feedback channel, allowing the users to report issues with data quality as well as with application functionality, they may encounter while interacting with PARTHENOS Discovery. Each page in PARTHENOS Discovery features a Feedback link that points to creating a New Issue in this git-repository, with the context page already prefilled.

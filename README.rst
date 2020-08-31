Scholars Articles Clustering
############################

What has been published concerning research and development and evaluation efforts of vaccines and therapeutics?

Given the large number of literature and the rapid spread of COVID-19, it is
difficult for health professionals to keep up with new information on the virus
and to have a good overview of what researcher did about vaccines and
therapeutics with coronaviruses.

This is a research repository for Clustering similar scholars articles in order to help decision makers to
have a glimpse of researches up to today.

By clustering and analyzing the specific scholars articles that answers the scientific community’s questions about vaccines and therapeutics,
we can help decision makers to understand the current state of research.


Scientific community’s questions:

Prevention for healthcare workers:

- Efforts to develop prophylaxis clinical studies and prioritize in healthcare workers

Therapeutics:

- Effectiveness of drugs being developed and tried to treat COVID-19 patients.
- Clinical and bench trials to investigate less common viral inhibitors against COVID-19 such as naproxen, clarithromycin, and minocyclinethat that may exert effects on viral replication.
- Capabilities to discover a therapeutic (not vaccine) for the disease, and clinical effectiveness studies to discover therapeutics, to include antiviral agents.

Vaccine:

- Methods evaluating potential complication of Antibody-Dependent Enhancement (ADE) in vaccine recipients.
- Exploration of use of best animal models and their predictive value for a human vaccine.
- Efforts targeted at a universal coronavirus vaccine.
- Approaches to evaluate risk for enhanced disease after vaccination
- Assays to evaluate vaccine immune response and process development for vaccines, alongside suitable animal models [in conjunction with therapeutics]

Distribution:

- Alternative models to aid decision makers in determining how to prioritize and distribute scarce, newly proven therapeutics as production ramps up. This could include identifying approaches for expanding production capacity to ensure equitable and timely distribution to populations in need.


.. contents::

.. section-numbering::

Data Collection
===============

- We are using datasets from COVID-19 Open Research Dataset Challenge (CORD-19).
(~50K, 19/04): https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge/tasks?taskId=561

Download Data
-------------

.. code-block:: bash

   cd ScholarsArticlesClustering/data
   wget "https://storage.googleapis.com/kaggle-data-sets/551982%2F1447747%2Fcompressed%2Fmetadata.csv.zip?GoogleAccessId=gcp-kaggle-com@kaggle-161607.iam.gserviceaccount.com&Expires=1599114568&Signature=MmD5REpggpTll%2BrXN4B81v0dqCeKwiRlGQ0QDc%2Btuy3VPt4Bt%2Ffg5414SgnAlv%2BUpD2B4%2B2nl0nPN3aktDNnnQ0NlCztwgPxgh8AzReQJS0fDZQEcabXDu2jkV%2BTZN73oFWKqBEYsbOcvVuml8XS%2BnC5yRMpXXfKdgE4V%2FKKQnTrY337K%2BiNnwxwtjAgcHMzu%2F%2F95FbMtbZauG6hd0YAgfNo5fr3MA2cjRQHZzmMlLRXY72841ZHawZNz3Vm%2BwH5tMx3r9RU00uPaoCKSNVUhJRdCAITYhLoxnHSCb9nX1IdSGxqWNOxposXwiLXK%2BUPfgbYeQswoDSVaU0FYZ3B%2Bg%3D%3D" -O temp.zip
   unzip temp.zip
   rm temp.zip

Solution
========

- Filtering & Cleaning: Focus on scholars about coronavirus. (W2V)

- Vectorization: Have a good representation of our articles on a vectors space.
(Bio RoBERTa)

- Clustering: Separate it by distance calculations or clustering algorithms.
(K-Means & K-NN)

- Insights Generation: Extract insights. (SciSpacy NER, Summarization
with BART, TextRank Keywords)

- Visualization: Create a dashboard (Widgets)

Dashboard Example
==============

.. image:: https://github.com/DataforGoodIsrael/ScholarsArticlesClustering/blob/master/notebooks/results/dashboard_example.png


Installation
============

.. code-block:: bash

  pip install -r requirements.txt

You have to use the notebooks in order, they are all connected.

Contributing
============

Author and current maintainer are the Data For Good Team.

You are more than welcome to approach us for help.

Contributions are very welcomed.


Improvement and Next Steps
==========================


- Collect more data up to date, creating an automatic data workflow.
- Create a package for the final models used based on this reasearch repository.
- Creating an interaction dashboard on a webapp.


Installing for development
==========================

Clone:

.. code-block:: bash

  git clone https://github.com/DataforGoodIsrael/ScholarsArticlesClustering.git


Credits
=======
Created by Samuel Jefroykin from Data For Good Israel

Contact us at hello@dataforgoodisrael.com

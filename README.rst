===============================================
Google / Bing / Baidu Search Results in Python
===============================================

.. image:: https://travis-ci.org/serpapi/google-search-results-python.svg?branch=master
    :target: https://travis-ci.org/serpapi/google-search-results-python

This Python package is meant to scrape and parse Google, Bing, Baidu results using `SerpAPI <https://serpapi.com>`_. 
The following services are provided:

* `Search API <https://serpapi.com/search-api>`_ 
* `Search Archive API <https://serpapi.com/search-archive-api>`_
* `Account API <https://serpapi.com/account-api>`_ 
* `Location API <https://serpapi.com/locations-api>`_

SerpApi provides a `script builder <https://serpapi.com/demo/>`_ to get you started quickly.

Feel free to fork this repository to add more backends.

Installation
-------------

Compatible with Python 2.7 or 3.7. 

.. code-block:: shell

    pip install google-search-results

`Link to the python package page <https://pypi.org/project/google-search-results>`_

Quick start
-------------

.. code-block:: python

    from lib.google_search_results import GoogleSearchResults
    client = GoogleSearchResults({"q": "coffee", "location": "Austin,Texas", "api_key": "secretKey"})
    result = client.get_dict()

This example runs a search about "coffee" using your secret api key.

The Serp API service (backend)

* searches on Google using the client: q = "coffee"
* parses the messy HTML responses
* return a standardizes JSON response

The GoogleSearchResults class

* Format the request
* Execute GET http request against Serp API service
* Parse JSON response into a dictionary

Et voila..

Alternatively, you can search:

* Bing using BingSearchResults class
* Baidu using BaiduSearchResults class

See the `playground to generate your code. <https://serpapi.com/playground>`_

`Documentation available here <https://github.com/serpapi/google-search-results-python/blob/master/README.md>`_

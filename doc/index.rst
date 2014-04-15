.. vim: set fileencoding=utf-8 :
.. Andre Anjos <andre.anjos@idiap.ch>
.. Mon  4 Nov 20:58:04 2013 CET

.. testsetup:: *

   import xbob.db.iris

======================
 Iris Flower Data Set
======================

.. todolist::

The `Iris flower data set <http://en.wikipedia.org/wiki/Iris_flower_data_set>`_
or Fisher's Iris data set is a multivariate data set introduced by Sir Ronald
Aylmer Fisher (1936) as an example of discriminant analysis. The dataset
consists of 50 samples from three species of Iris flowers (Iris setosa, Iris
virginica and Iris versicolor). Four features were measured from each sample,
they are the length and the width of sepal and petal, in centimeters.

As this data set is quite small and used for testing purpose, it is directly
integrated into |project|, which provides both ways to access the data, as well
as the data itself (feature vectors of length four for various samples of the
three species).

A description of the feature vector can be obtained using the attribute
:py:attr:`xbob.db.iris.names`.

.. doctest::
   :options: +NORMALIZE_WHITESPACE, +ELLIPSIS

   >>> descriptor_labels = xbob.db.iris.names
   >>> descriptor_labels
   ['Sepal Length', 'Sepal Width', 'Petal Length', 'Petal Width']

The data (feature vectors) can be retrieved using the
:py:meth:`xbob.db.iris.data()` function. This returns a 3-key dictionary, with
3 :py:class:`numpy.ndarray` as values, one for each of the three species of
Iris flowers.

.. doctest::
   :options: +NORMALIZE_WHITESPACE, +ELLIPSIS

  >>> data = xbob.db.iris.data()
  >>> type(data['setosa'])
  <... 'numpy.ndarray'>
  >>> data['setosa'].shape
  (50, 4)
  >>> list(data.keys())
  [...]

Each :py:class:`numpy.ndarray` consists of 50 feature vectors of length four.

The database also contains statistics about the feature vectors, which can be
obtained using the :py:attr:`xbob.db.iris.stats` dictionary. A description
of these statistics is provided by :py:attr:`xbob.db.iris.stat_names`.

References
----------

.. automodule:: xbob.db.iris

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. include:: links.rst

.. Place here your external references


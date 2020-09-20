####################
IS 210 Assignment 05
####################
************
Warmup Tasks
************

:College: CUNY School of Professional Studies
:Course-Name: Software Application Programming I
:Course-Code: IS 210

Overview
========

This lesson introduces basic list and tuple construction as well as
touching upon some key list functions.

Instructions
============

The following tasks will either have you interacting with existing files in
the assignment repository or creating new ones on the fly. Don't forget to add
your interpreter directive, utf-8 encoding, and a short docstring with any new
files that you create!

.. important::

    In these exercises, you may, on occasion, come across a task that requres
    you to research or use a function or method not directly covered by the
    course text. Since Python is such a large language it would be impossible
    for the author to have included descriptions of each and every available
    function which would largely duplicate the offical Python documentation.

    A *vital* skill to successful programming is being comfortable searching
    for and using official language documentation sources like the
    `Python String Documentation`_ page. Throughout our coursework we will be
    practicing both the use of the language in practice and the search skills
    necessary to become functional programmers.

Warmup Tasks
============

Task 01
-------

In this first task, you'll be statically defining a list and a tuple using
their standard constructors.

Specifications
^^^^^^^^^^^^^^

1.  Open a new Jupyter notebook

2.  create a constant named ``ELEMENTS`` and set its values
    to a ``tuple()`` with the following data (in order):

    0.  ``None`` (the Python constant, not a string)

    1.  ``Hydrogen``

    2.  ``Helium``

    3.  ``Lithium``

    4.  ``Beryllium``

    5.  ``Boron``

    6.  ``Carbon``

3.  Create a list named ``OPERATIONS_ORDER`` and assign it the following
    data, in-order:

    0.  ``Parentheses``

    1.  ``Exponents``

    2.  ``Multiplication``

    3.  ``Division``

    4.  ``Addition``

    5.  ``Subtraction``

4.  Print the results as shown below

Expected Output
^^^^^^^^

.. code:: pycon

    >>> ELEMENTS
    (None, 'Hydrogen', 'Helium', 'Lithium', 'Beryllium', 'Boron', 'Carbon')
    >>> OPERATIONS_ORDER
    ['Parentheses', 'Exponents', 'Multiplication', 'Division', 'Addition',
    'Subtraction']


Task 02
-------

Looping lists with a ``for`` loop is a powerful and straightforward way to
process huge blocks of data at the same time. Here, we'll explore this concept
with our ``data`` module.

Specifications
^^^^^^^^^^^^^^

1.  Use the same Jupyter notebook
    
2.  Create a new function named ``process_data()`` that takes one argument:

    1.  ``data``, a list or tuple of numbers.

3.  Use a ``for`` loop to loop through the data and return a tuple
    containing the follow data points in-order:

    1.  The total sum of the data

    2.  The average of the data with floating point precision

4.  Run the function as shown below in "Expected Output"

.. hint::

    Avoid repetition at all costs and remember that repetition inside of a
    loop is still repetition even if the code itself is not repeated.

.. hint::

    You should first create your total outside of the loop so you can add to
    it as the loop is processing.

Expected Output
^^^^^^^^

.. code:: pycon

    >>> process_data([1, 2, 3])
    (6, 2.0)

.. tip::

    Check out the ``data`` module for a few functions that return a huge

    number of records and watch your

Task 03
-------

Our last warmup task will touch upon the mutability differences between
strings and their cousin, the tuple.

Specifications
^^^^^^^^^^^^^^

1.  Use the same Jupyter notebook

2.  Create a function named ``flip_keys()`` that takes one argument:

    1.  A list named ``to_flip``. This list is assumed to have nested,
        immutable sequences inside it, eg: ``[(1, 2, 3), 'hello']``

3.  Use a ``for`` loop to loop the list and reverse the order of the
    inner sequence. All operations on the outer list must operate on the
    original object, taking advantage of its mutability. Inner elements are
    immutable and will require replacement.

4.  The function should return **the original list** with its inner elements
    reversed.
    
5.  Run the test below and show the expected output in your notebook
    
.. warning:

    Your tests will fail if you try to create a new list and return that.
    You must return the original input object and modify it on-the fly
    in your loop.
    
.. hint::

    Consider how to access or change the value of a list. You did it already
    in task 2!

.. hint::

    In order to change the value in ``to_flip`` you'll need some way to know
    which index you're attempting to change. To do-this, create a variable
    to act as a counter and increment it within your loop, eg:

    .. code:: python

        counter = 0
        for value in iterable_object:
        # do something
        counter += 1
        
    Now consider what that counter could represent. At the end of this loop
    does ``counter == len(iterable_object)``

.. hint::

    For an idea on how to reverse a tuple, head back to an earlier assignment
    when you reversed a string using the slice syntax.

Expected Output
^^^^^^^^

.. code:: pycon

    >>> LIST = [(1, 2, 3), 'abc']
    >>> NEW = flip_keys(LIST)
    >>> LIST is NEW
    True
    >>> print LIST
    [(3, 2, 1), 'cba']



Submission
==========

Code should be submitted via Blackboard as a single Jupyter notebook file.

In order to receive full credit you must complete the assignment as-instructed and without any violations (reported in the build status).

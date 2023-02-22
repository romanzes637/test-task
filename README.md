# test-task

## Data (See data directory for examples)
Object ``A``
* ``value`` (float)
* ``color`` (str)

Object ``B``
* ``function`` (str)
* ``value`` (float)

Object ``C``
* ``value`` (list of float)

## Tasks
1. Create a database (``DB``) to store objects ``A``, ``B`` and ``C`` each in a 
separate table
2. Implement a function that takes ``A`` and ``B`` and return ``C``, where 
``B.function`` applies to ``A.value`` and ``B.value`` and the result is stored in 
``C.value`` with an index that depends on ``A.color`` according to the map:

``COLOR 2 INDEX MAP``
* ``red`` -> ``0``
* ``green`` -> ``1``
* ``blue`` -> ``2``

Example 1
``INPUT`` (``A``, ``B``)
* ``A.value`` = ``3``
* ``A.color`` = ``green`` 
* ``B.function`` = ``sum`` 
* ``B.value`` = ``3`` 
``OUTPUT`` (``C``)
* ``C.value`` = ``[ 0, 6, 0 ]``

Example 2
``INPUT`` (``A``, ``B``)
* ``A.value`` = ``2``
* ``A.color`` = ``red`` 
* ``B.function`` = ``pow`` 
* ``B.value`` = ``2`` 
``OUTPUT`` (``C``)
* ``C.value`` = ``[ 4, 0, 0 ]``

3. Implement a function similar to function-2 but with ``INPUT`` from ``DB`` and ``OUTPUT`` to ``DB``
4. Add REST endpoints to function-2 and function-3
5. Wrap it all up in a Docker container (i.e. write ``Dockerfile`` and ``docker-compose.yaml``)
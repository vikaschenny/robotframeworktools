============
times2csv.py
============

``times2csv.py`` is a tool for creating a CSV file containing
suite, test and keyword execution times (start/end/elapsed time).

Synopsis
--------

.. sourcecode:: bash

  $ times2csv.py input-xml [output-csv] [include-items]

Description
-----------

Robot Framework Start/End/Elapsed Time Reporter

This script reads start, end, and elapsed times from all suites, tests and/or
keywords from the given output file, and writes them into a file in
comma-separated-values (CSV) format. CSV files can then be further processed
with spreadsheet programs. If the CSV output file is not given, its name is
got from the input file by replacing the *.xml* extension with *.csv*.

'include-items' can be used for defining which items to process. Possible
values are 'suite', 'test' and 'keyword', and they can be combined to specify
multiple items e.g. like 'suite-test' or 'test-keyword'.

Examples
--------

.. sourcecode:: bash

   $ times2csv.py output.xml
   $ times2csv.py path/results.xml path2/times.csv
   $ times2csv.py output.xml times.csv test
   $ times2csv.py output.xml times.csv suite-test

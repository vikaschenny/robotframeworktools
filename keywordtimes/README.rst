===============
keywordtimes.py
===============

This is a tool that helps you to profile where the most of the time in your test cases is consumed.
This is helpful for example in situations where you want to optimise the test execution times.

.. sourcecode:: bash

   $ keywordtimes.py [input file output.xml]

   Example output:

   Total time (s) | Number of calls | avg time (s) | median time (s) | standard deviation (s) | Keyword name
            0.612 |               2 |        0.306 |           0.306 |                    0.0 | "Some Keyword"
            0.606 |               4 |        0.151 |           0.151 |                   0.05 | "BuiltIn.Sleep"
            0.406 |               2 |        0.203 |           0.203 |                    0.0 | "Other Keyword"
   Showing 100 of total keywords 3


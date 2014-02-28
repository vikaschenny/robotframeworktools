===============
keywordtimes.py
===============

.. sourcecode:: bash

   usage: keywordtimes.py [-h] [--limit LIMIT] [--show SHOW] source

   This is a tool that helps you to profile where the most of the time in your
   test cases is consumed. This is helpful for example in situations where you
   want to optimise the test execution times.

   positional arguments:
      source                output from a Robot Framework execution to analyze
  
   optional arguments:
      -h, --help            show this help message and exit
      --limit LIMIT, -l LIMIT
                            Filter out keywords with larger percentage of
			    stdev/avg time than LIMIT. This helps by filtering out
	                    most used "primitive" keywords such as Sleep and Run
                            Keyword If etc. and let's you focus on the keywords
                            that very often take a lot of time to execute (in
                            other words are most fruitful places to focus
			    optimisation effort).
      --show SHOW, -s SHOW  Max number of shown keywords. Default is 100.

   Example output:
   
   Total time (s) |   Calls | avg time (s) | median time (s) | stdev (s) | stdev/avg time % | Keyword name
            49.13 |       2 |       24.565 |          24.565 |     0.841 |             3.42 | "atest_resource.Run Tests"
            49.13 |       2 |       24.565 |          24.565 |     0.841 |             3.42 | "atest_resource.Run Tests Helper"
           49.098 |       2 |       24.549 |          24.549 |     0.841 |             3.43 | "atest_resource.Run Helper"
           49.068 |       2 |       24.534 |          24.534 |     0.826 |             3.37 | "OperatingSystem.Run And Return Rc"
           25.406 |       1 |       25.406 |          25.406 |       0.0 |              0.0 | "Run Tests With Listeners"	 
 	    0.032 |       2 |        0.016 |           0.016 |       0.0 |              0.0 | "atest_resource.Set Variables And Get Datasources"
            0.016 |       2 |        0.008 |           0.008 |     0.008 |            100.0 | "atest_resource.Set Variables"
	    0.016 |       1 |        0.016 |           0.016 |       0.0 |              0.0 | "BuiltIn.Evaluate"
            0.016 |       1 |        0.016 |           0.016 |       0.0 |              0.0 | "atest_resource.Get Output File"
            0.016 |       1 |        0.016 |           0.016 |       0.0 |              0.0 | "atest_resource.Stderr Should Be Empty"
	    0.016 |       1 |        0.016 |           0.016 |       0.0 |              0.0 | "atest_resource.Get Stderr"
	    0.015 |      10 |        0.002 |             0.0 |     0.004 |            200.0 | "BuiltIn.Log"


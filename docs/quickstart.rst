
Quickstart
==========

This example loads the sample measurements included with ``ci_course``,
calculates summary statistics for each measurement column, and writes a
plain-text report. Complete the :doc:`install` instructions first.

Using Python
------------

Create a file named ``example.py`` in the repository root with the following
contents:

.. code-block:: python

   from ci_course import load_measurements, summarise_all, write_report

   # Load the sample CSV file bundled with the package.
   measurements = load_measurements()

   # Calculate summary statistics for each measurement column.
   summaries = summarise_all(measurements)

   # Display the results in the terminal.
   for name, summary in summaries.items():
       print(f"{name}: {summary}")

   # Save a formatted plain-text report.
   report_path = write_report(summaries, "report.txt")
   print(f"Report written to {report_path}")

Run the script from the repository root:

.. code-block:: console

   python example.py

The ``load_measurements()`` function reads the bundled
``sample_measurements.csv`` file. ``summarise_all()`` calculates the count,
mean, sample standard deviation, minimum and maximum for each measurement
column, ignoring missing values. ``write_report()`` saves these results to
``report.txt`` in your current directory.

Using the command line
----------------------

You can also run the same workflow without writing a Python script:

.. code-block:: console

   ci-course

This prints the sample-data summary. To save it to a file instead, run:

.. code-block:: console

   ci-course -o report.txt

To summarise your own CSV file, pass its path:

.. code-block:: console

   ci-course measurements.csv -o report.txt

The CSV should have column headers. If present, ``sample_id`` is treated as
an identifier; other columns should contain numeric measurements or blank
cells for missing values.

For details of the available Python functions, see the :doc:`reference`.

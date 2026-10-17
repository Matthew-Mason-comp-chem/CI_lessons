
Installation
============

The ``ci_course`` package summarises experimental measurements stored in CSV
files and can produce a plain-text report. It requires Python 3.12 or newer.

Get the code
------------

Clone the repository and enter the project directory:

.. code-block:: console

   git clone https://github.com/Matthew-Mason-comp-chem/CI_lessons.git
   cd CI_lessons

Create a virtual environment
----------------------------

On macOS or Linux:

.. code-block:: console

   python3 -m venv venv
   source venv/bin/activate

On Windows (PowerShell):

.. code-block:: powershell

   python -m venv venv
   .\venv\Scripts\Activate.ps1

Install the package
-------------------

Install the package and the dependencies used in the course:

.. code-block:: console

   python -m pip install -e ".[dev,docs]"

The ``-e`` option installs the package in editable mode, so edits to the
source code are available without reinstalling it.

Check the installation
----------------------

Run the command-line tool on its bundled sample dataset:

.. code-block:: console

   ci-course

You should see a measurement summary printed in the terminal.

Next, follow the :doc:`quickstart` to create a report file.

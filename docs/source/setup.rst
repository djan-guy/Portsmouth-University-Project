Setup
==============

This page is dedicated to Setup.

.. code-block:: python

    def retrieveIncomes():
        connection = sqlite3.connect("taxcalculator.db")
        cursor = connection.cursor()
        cursor.execute("SELECT * FROM Incomes")
        rows = cursor.fetchall()
        for row in rows:
            print(row)

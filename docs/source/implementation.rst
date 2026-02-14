Implementation
==============

This page is dedicated to Implementation.

More on the data persistence code:

.. code-block:: python
     :linenos:
    def retrieveIncomes():
        connection = sqlite3.connect("taxcalculator.db")
        cursor = connection.cursor()
        cursor.execute("SELECT * FROM Incomes")    
        rows = cursor.fetchall()
        for row in rows:
            print(row)
        return rows
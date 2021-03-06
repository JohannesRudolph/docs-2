﻿# Ongoing Tasks: Testing ETL Scripts 
---

{NOTE: }

* ETL transformations can be tested with the usage of `Test script` option. Edit your script in the Studio to enter test mode.

* In this page:  
  * [Testing Raven ETL Scripts](../../../server/ongoing-tasks/etl/test-scripts#testing-raven-etl-scripts)  
  * [Testing SQL ETL Scripts](../../../server/ongoing-tasks/etl/test-scripts#testing-sql-etl-scripts)  
{NOTE/}


{PANEL: Testing Raven ETL Scripts}

![Figure 1. Test RavenDB ETL script](images/test-raven.png "Test RavenDB ETL script")

{NOTE: }

* In order to test your transformation script you need to:

 1. Enter ID of a document that will be used.
 2. Choose the test mode:
    - `Document put / update` - use to see script results when the document is created or modified.
    - `Document delete` - use to see script results when the document is deleted (note that [delete behavior functions](../../../server/ongoing-tasks/etl/raven#deletions) can be called then).
 3. Click `Test` button.


    After executing the script in test mode you'll see the following tabs:

 4. `Document Preview` displays the original document used in the test.
 5. `Test Results` presents the list of commands that will be sent to a destination database.
 6. `Debug output` contains all debug outputs that were created using `output()` function called in the script body. The function accepts string parameter.

{NOTE/}

{PANEL/}


{PANEL: Testing SQL ETL Scripts}

![Figure 2. Test SQL ETL script](images/test-sql.png "Test SQL ETL script")

{NOTE: }

* Testing SQL transformations requires the same steps as testing Raven ETL. Although there is one additional option available, `Execute and rollback the test transaction`:

  - unchecked (default): no execution of SQL statements will take place, will only show generated SQL statements,
  - checked: all generated SQL statements will be executed against the target SQL database, the transaction will be rolled back when done.

* The test results displayed in `Test Results` are SQL statements that would be sent to relational database. Depending on `Execute and rollback the test transaction` option they
will be parametrized (option checked) or values will be inserted directly into statements (option unchecked).

{NOTE/}

{PANEL/}

Setup Thread Group:
It is a special form of Thread Group used to perform necessary actions before execution of regular thread group starts. Behavior of threads mentioned under Setup Thread Group is exactly same as normal thread group.

setup_threadgroup
Purpose of having Setup Thread Group is to distinguish all pre-test actions from the normal thread group so they can be performed before the actual test execution starts. Jmeter automatically triggers Setup Thread group before normal one.

Example:
1) Import amount of Data from Database and store them into variables.
2) Create / Register multiple users to be used in Test Thread Group.

TearDown Thread Group:
It is a special form of Thread Group used to perform necessary actions after the execution of regular thread group completes. Behavior of threads mentioned under Setup Thread Group is exactly same as normal thread group.

Teardown Thread Group
Use of TearDown Thread Group is to differentiate all the post-test actions which are required to run once the execution of normal thread group is over. Jmeter will automatically trigger TearDown Thread Group after execution of regular thread group completes.

Note:
By default, TearDown Thread Group won’t run if the Test is completed as expected. If you want to run it anyway, mark the check-box “Run tearDown Thread Groups after shutdown of main threads” from Test Plan element.

Example:
1) Delete Users which were created in beginning of the test.

In the mentioned JMX file Users will be created in setup threadgroup based on thread user number and those users will be write in to a csv file. 
In the next thread group, we will just login with those users after reading from csv
Teard down thread group will delete the users.

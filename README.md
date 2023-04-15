# Executives_Nprinting

# Simulation



<h2>Description</h2>
Presented here is an executive dashboard (also in table version) which is sent every month automatically using Nprinting. 
The executive dashboard will be sent only when the "working hours" file (an excel file) will be updated.

<br />
<h3>The Dashboard:</h3>
<br />
<a href="https://ibb.co/M5fjML2"><img src="https://i.ibb.co/1JMp8xv/Picture1.png" alt="Picture1" border="0"></a><br />

<h4>Due to requests in the organization, a table version has also been created:</h4>

<a href="https://ibb.co/xgYdmPX"><img src="https://i.ibb.co/5jkwYtG/Picture8.png" alt="Picture8" border="0"></a><br />
<br />
Once the dashboard and the table were created in the GUI, it was necessary to think of a way to send these as a report directly to the organization's executives using Nprinting add-on module. The report should be sent every month and it was not possible to simply set a fixed monthly date for sending because some measures in this report depend on the amount of monthly working hours in the organization.
The working hours are currently saved in an Excel file which is updated every month (but not necessarily on the same day of the month). 
To avoid a situation where the report will be sent automatically before the working hours have been updated (and as a result part of the report will not be displayed correctly) The idea was that the report would only be sent after an update was made to the working hours file.

For this purpose, the following were done:

<br />
<h2>Creating the dashboard:</h2>
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/FJKgq5j/Picture6.png" alt="Picture6" border="0"></a>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

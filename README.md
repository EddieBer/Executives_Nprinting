# Executives_Nprinting

<h2>Description</h2>
Presented here is an executive dashboard (also in table version) which is sent every month automatically using Nprinting. 
The executive dashboard will be sent only when the "working hours" file (an excel file) will be updated.

<br />
<h3>The Dashboard:</h3>

<a href="https://ibb.co/M5fjML2"><img src="https://i.ibb.co/Yd6QbkT/Dashboard.png" alt="Picture1" border="0"></a><br />
<br />
<h4>Due to requests in the organization, a table version has also been created:</h4>

<a href="https://ibb.co/xgYdmPX"><img src="https://i.ibb.co/1M1gL3Z/Picture1.png" alt="Picture8" border="0"></a><br />
<br />
Once the dashboard and the table were created in the GUI, it was necessary to think of a way to send these as a report directly to the organization's executives using Nprinting add-on module. The report should be sent every month and it was not possible to simply set a fixed monthly date for sending because some measures in this report depend on the amount of monthly working hours in the organization.
The working hours are currently saved in an Excel file which is updated every month (but not necessarily on the same day of the month). 
To avoid a situation where the report will be sent automatically before the working hours have been updated (and as a result part of the report will not be displayed correctly) The idea was that the report would only be sent after an update was made to the working hours file.

For this purpose, the following were done:

1. Defining the logic in the script (Data Load Editor) which says that only if a change is    detected in the working hours file (the excel file) than the QVD files      (C1+C2) must be updated. In addition, it can be seen that a number of variables have been set (vt_year, vt_month, vt_day) which together indicate the date when the    QVD files were last updated and which we will use later in the GUI:

<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/cgvYcdR/Picture5.png" alt="Picture5" border="0"></a>
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/GRqq9Mj/Picture6.png" alt="Picture6" border="0"></a>
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/0CMg879/Picture7.png" alt="Picture7" border="0"></a>

2. In the GUI we have set the table to only be displayed if the QVD files have been updated and
if it is the same as today's date, by creating a new variable called vDate_UI which consists of the variables we defined in the Script:
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/SmMXk6Z/Picture1.png" alt="Picture1" border="0"></a>
<br />
And finally the condition for displaying the table:
<br />
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/c83G6s4/Picture2.png" alt="Picture2" border="0"></a>
<br />
<br />
3. In Nprinting we created a QlikEntity report for the dashboard and for the table (We chose the QlikEntity type mainly because the report can be displayed as an image directly in the email and not just as an attachment that needs to be opened separately):
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/5MMFJFR/Picture3.png" alt="Picture3" border="0"></a>

4. Finally, we defined a Task that will be executed only when a condition is met in which the object (chart) of the table is displayed properly 
(which actually means that there was an update in the excel file of the working hours file and Nprinting can send the updated executive's report):
<a href="https://ibb.co/vmHZv3K"><img src="https://i.ibb.co/HqBRCjc/Picture4.png" alt="Picture4" border="0"></a>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

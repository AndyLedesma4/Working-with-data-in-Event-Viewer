# Working-with-data-in-Event-Viewer
<!--Prerequisites and Installation--> 
This tutorial outlines the steps for analyzing events in Event Viewer.<br /> 

<!--Products or Software used--> 
<h2>Environments and Technologies Used</h2> 
- Event Viewer<br /> - Windows 10 (21H2) <br />
<h2>STEPS INCLUDED</h2> <h3>Step 1: Open Event Viewer</h3>
1. Open Event Viewer.
<br /> 2. In the left pane, click the Custom Views arrow and then click 
<b>Administrative Events</b>. 
A list of Administrative Events appears in the center pane of the Event Viewer window. This log lists Critical, Error, and Warning events.<br />
<br /> 
<h3>Step 2: Find DHCP-Related Events</h3> 1. In the <b>Actions</b> 
pane (the pane on the right), in the <b>Administrative Events</b> 
section, click <b>Find</b>. 
The Find dialog box opens.<br /> 2. In the <b>Find what</b> text box, type <code>dhcp</code>, and then click <b>Find Next</b>. <br />

<h3>Step 3: Attach Task to Event</h3> 1. Click <b>Cancel</b> to close the Find dialog box. Keep the event listing that you found highlighted.<br />
2. In the <b>Actions</b> pane, click <b>Attach Task To This Event</b>.
The Create Basic Task Wizard dialog box opens.<br /> 3. In the <b>Name</b> text box, replace the default text with <code>DHCP_my_computer</code> or some other text appropriate for the type of event you’re saving. Click <b>Next</b> to continue.<br />
4. Confirm the Log, Source, and Event ID for this error and click <b>Next</b> to continue.<br /> 
5. Select <b>Start a program</b> as the action to take when this error occurs. Click <b>Next</b> to continue.<br /> 
6. Click the <b>Browse</b> button and find the <code>cmd.exe</code> file, located in <code>C:\\Windows\\System32\\cmd.exe</code>. Select the file and click <b>Open</b>. Click <b>Next</b> to continue.<br /> 
7. Review the summary of your notification selections and click <b>Finish</b> to create the task.<br /> <h3>Step 4: Verify Task in Task Scheduler</h3> 
1. Press <code>Win+R</code> and enter <code>taskschd.msc</code>.<br /> 
2. In the Task Scheduler window, click the down arrow next to <b>Task Scheduler Library</b>, then click <b>Event Viewer Tasks</b>. Select the task you just created.<br />

<h3>Step 5: Clean Up</h3> You can now delete this task if you want. Close all open windows.
<br />

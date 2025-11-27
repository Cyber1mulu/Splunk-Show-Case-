<h3> Splunk Dashboard for Web Traffic Logs </h3>

<h3>Object</h3>

<h3>Lab Set Up </h3>

<h5> Task 1 The First one setting up Time Range </h5>

  -Add Time Range Button

  -Click on Add Input

  -Select Time and click on pencil icon

  -Set Label to Time Range and Token time_range

  -Again Add Input

  -Select Submit
  
<h5>Task2: Web Activities

  Goal: Give a quick summary of Web activity. </h5>
  
   Web Requests
  Click on Add Panel
  Under New, choose Single Value
  Use Shared Time Picker time_range
  Set Content Title to "Total Web Requests"
  Enter the Search String as below
 

<table>
   <thead>
        
     pache_mixed_acess_full (1).json" host="webserver" sourcetype="_json"
        | stats count AS "Total Web Requests"
   </thead>
</table>

       




Splunk Dashboard for Web Traffic Logs

Object

Lab Set Up

Task 1 The First one setting up Time Range

  -Add Time Range Button

  -Click on Add Input

  -Select Time and click on pencil icon

  -Set Label to Time Range and Token time_range

  -Again Add Input

  -Select Submit


Task1: Web Activities

  Goal: Give a quick summary of Web activity.
 1  <h4>Total Web Requests</h4>
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

       




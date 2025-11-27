<h3> Splunk Dashboard for Web Traffic Logs </h3>

<h3>Object</h3>

<h3>Lab Set Up </h3>

<h5> Task 1 First setting up Time Range </h5>

  1 Add Time Range Button
  - Click on Add Input
  - Select Time and click on pencil icon
  - Set Label to Time Range and Token time_range
  - Again Add Input
  - Select Submit
  
<h5>Task2: Web Activities

  Goal: Give a quick summary of Web activity. </h5>
  
  2 Web Requests
  - Click on Add Panel
  - Under New, choose Single Value
  - Use Shared Time Picker time_range
  - Set Content Title to "Total Web Requests"
  - Enter the Search String as below
 

<table>
   <thead>
        
    source=pache_mixed_acess_full (1).json" host="webserver" sourcetype="_json"
        | stats count AS "Total Web Requests"
   </thead>
</table>

3 Successful Response

- Click on Add Panel
- Under New, choose Single Value
- Use Shared Time Picker time_range
- Set Content Title to "Successful Response"
- Enter the Search String as below
       
<table>
   <thead>
        
    source="apache_mixed_access_full (1).json" host="webserver" sourcetype="_json" method=GET status=200 
    | stats count AS "Successful Responses"	
   </thead>
</table>

4 Client Errors
- Click on Add Panel
- Under New, choose Single Value
- Use Shared Time Picker time_range
- Set Content Title to "Client Errors"
- Enter the Search String as below:

<table>
   <thead>


       source="apache_mixed_access_full (1).json" host="webserver" sourcetype="_json" 
       | where status>=400 and status<500 
       | stats count AS "Client Errors"
      
   </thead>
</table>

5 Server Errors 
- Click on Add Panel
- Under New, choose Single Value
- Use Shared Time Picker time_range
- Set Content Title to "Server Errors (5xx)"
- Enter the Search String as below:

<table>
   <thead>

  source="apache_mixed_access_full (1).json" host="webserver" sourcetype="_json" 
  | where status>=400 and status<500 
  | stats count AS "Client Errors"
     
   </thead>
</table>

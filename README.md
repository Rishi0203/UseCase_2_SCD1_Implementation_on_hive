<h1>SCD Type 1 Implementation on hive</h1>

<h4>Slowly Changing Dimensions (SCD)</h4> 
<p>dimensions that change slowly over time, rather than changing on regular schedule, time-base.</p>

<h4>Slowly Changing Dimensions (SCD) Type 1 </h4>
<p> Overwriting the old value. In this method no history of dimension changes is kept in the database. The old dimension value is simply overwritten be the new one. This type is easy to maintain and is often use for data which changes are caused by processing corrections(e.g. removal special characters, correcting spelling errors).</p>

<h4>Desciption </h4> 

<p>Here, client Told that requirement read data from CSV and load on mysql and after that export data from mysql to HDFS and after that create a hive table and save data in file partition by Year, Month and Day and do Implementation SCD Type 1 on that, after done load data on table check no of record is accurate or not.</p>

<h4>MySQL Table</h4> 
<table>
<tr>
 <th>Field </th> 
  <th>Type </th> 
  <th>Key  </th> 
 </tr>
  <tr>
     <td> custid  </td> <td>int </td> <td>PRI  </td> 
 </tr>  
  <tr>
     <td> username  </td> <td> varchar(100) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> quote_count   </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td> ip  </td> <td> varchar(50) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> entry_time  </td> <td> varchar(20) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> prp_1   </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td> prp_2  </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td> prp_3  </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td> ms  </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td> http_type    </td> <td> varchar(50) </td> <td>  </td> 
 </tr>  
  <tr>
     <td>  purchase_category  </td> <td> varchar(255) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> total_count  </td> <td>int </td> <td>  </td> 
 </tr>  
  <tr>
     <td>  purchase_sub_category  </td> <td> varchar(255) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> http_info    </td> <td> varchar(255) </td> <td>  </td> 
 </tr>  
  <tr>
     <td> entry_time_Day   </td> <td>int </td> <td>  </td> 
 </tr>
   <tr>
     <td> entry_time_Month     </td> <td>int </td> <td>  </td> 
 </tr>
   <tr>
     <td> entry_time_Year  </td> <td>int </td> <td>  </td> 
 </tr>
</table>


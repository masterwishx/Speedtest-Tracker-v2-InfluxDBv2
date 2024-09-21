# Speedtest-Tracker-v2-InfluxDBv2

A dashboard to display data exported by Speedtest Tracker v2 . Avalible Now at Grafana Dashboard 17808
(https://grafana.com/grafana/dashboards/17808-speedtest-tracker-v2-influxdbv2/)

This dashboard shows data collected by Speedtest Tracker v2 https://github.com/alexjustesen/speedtest-tracker and exported in an InfluxDBv2 database in the bucket.

Dashboard based on my previous dashboard Speedtest Tracker - InfluxDBv2 with guide for OLD Speedtest Tracker app. https://grafana.com/grafana/dashboards/16428-speedtest-tracker/

Same steps here as before for exporting data but without needs for influxDBv1.

## Steps
```
1. create bucket in InfluxDBv2

2.1 create or use exist API token (ALL ACCESS) for Grafana and auth.

2.2 create API token (read/write) for this bucket to use with speedtest-tracker or use exist.

3. Config Client of InfluxDBv2(Speedtest-tracker) by entered data : bucket, etc ...

4. Check in InfluxDBv2 in Data Explorer that data is exist in bucket

5. Then you can select all data needed and switch to Script Editor copy the script (already done)

6. Configure Grafana to use with data from InfluxDBv2 ( select datasource = InfluxDB , Query Language = Flux  ,Organization = yourorg , Bucket = speedtest , Token = yourtoken for bucket )

7. import this script in Grafana Dashboard .

8. Enjoy
```

![image](https://github.com/user-attachments/assets/25aeb76a-5acf-4135-8073-a61f6bcb8cc3)
![influxsetup](https://user-images.githubusercontent.com/28630321/187088939-492e8910-395b-4aef-b1f8-199ea98a2dc8.jpg)

## Info
![Screenshot 2024-08-14 202917](https://github.com/user-attachments/assets/aab1ed25-2e70-4486-b540-4da6306418b6)
![Screenshot 2024-08-14 202935](https://github.com/user-attachments/assets/37685a7d-9d58-4987-a4dd-2ebeabaebc49)

``` 14.8.24 - More Panels added + some fixes. ```<br>
``` 20.4.24 - Panels fixed + Avg Speed fixed. ```<br>
``` 6.4.24 - Added Multi bucket support. ```<br>

 You can change bucket name and add multiple buckets by : 

 <b>Go to Dashboard Setting - Variables - Click on bucket - Custom options:</b>
 
![Screenshot 2024-04-06 204806](https://github.com/masterwishx/Speedtest-Tracker-v2-InfluxDBv2/assets/28630321/808c1b36-71dc-4669-8014-6aac6ebfd85b)


 

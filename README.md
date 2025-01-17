# Speedtest-Tracker-v2-InfluxDBv2

A dashboard to display data exported by Speedtest Tracker v2 . Avalible Now at Grafana Dashboard 17808
(https://grafana.com/grafana/dashboards/17808-speedtest-tracker-v2-influxdbv2/)

This dashboard shows data collected by Speedtest Tracker v2 https://github.com/alexjustesen/speedtest-tracker and exported in an InfluxDBv2 database in the bucket.

Dashboard based on my previous dashboard Speedtest Tracker - InfluxDBv2 with guide for OLD Speedtest Tracker app. https://grafana.com/grafana/dashboards/16428-speedtest-tracker/

Same steps here as before for exporting data but without needs for influxDBv1. Check [Here](#steps)


## Info
![Screenshot 2024-08-14 202917](https://github.com/user-attachments/assets/aab1ed25-2e70-4486-b540-4da6306418b6)
![Screenshot 2024-08-14 202935](https://github.com/user-attachments/assets/37685a7d-9d58-4987-a4dd-2ebeabaebc49)

## Updates

``` 17.1.25 - Removed personalisations, reverted bucket variable to expected standard (speedtest-tracker-new,speedtest-tracker-cloud > speedtest-tracker), reverted IP:port to expected (9443>8443). Updated README.md for customisations. ```<br>
``` 8.12.24 - Fixed time in Latest result panel. ```<br>
``` 7.12.24 - Compatibility Update for Speedtest Tracker v0.25 some fields have been moved to tags + some fixes. ```<br>
``` 14.8.24 - More Panels added + some fixes. ```<br>
``` 20.4.24 - Panels fixed + Avg Speed fixed. ```<br>
``` 6.4.24 - Added Multi bucket support. ```<br>

## Multi buckets

 You can change bucket name and add multiple buckets (comma separated list):

 <b>Go to `Dashboard Setting > Variables > bucket > Custom options`:</b>
 
<img width="582" alt="Screenshot 2025-01-17 at 16 04 11" src="https://github.com/user-attachments/assets/e4173c4e-3456-45f9-9282-7f28daacf0c2" />
<img width="541" alt="Screenshot 2025-01-17 at 16 02 29" src="https://github.com/user-attachments/assets/55a0b9b2-2299-4fa8-962d-8db9533af0c2" />

## Custom Link

 You can update the link to your speedtest-tracker application:

 <b>Go to `Dashboard Setting > Links > Speedtest Tracker v2 App`:</b>
 
<img width="630" alt="Screenshot 2025-01-17 at 12 21 23" src="https://github.com/user-attachments/assets/99f49212-09a9-42eb-9697-d829ff0cd160" />


## Steps
```
1. Create bucket in InfluxDBv2: speedtest-tracker

2.1 Create or use existing API token (ALL ACCESS) for Grafana and auth.

2.2 Create API token (read/write) for this bucket to use with speedtest-tracker or use existing.

3. Configure Speedtest Tracker application with relevant InfluxDBv2 configuration: URL, org, bucket, token, etc..., and 'Test connection'

4. Check in InfluxDBv2 in Data Explorer that test data exists in bucket

5. Configure Grafana to use with data from InfluxDBv2 ( Select Datasource = InfluxDB , Query Language = Flux  ,Organization = yourorg , Bucket = speedtest-tracker , Token = yourtoken for bucket )

6. Import this dashboard to Grafana (Dashboard > New > Import) using link in README.md

7. Return to Speedtest Tracker application and Export data to InfluxDB (Settings > Data Integration > Export current results)

7. Enjoy
```

![image](https://github.com/user-attachments/assets/25aeb76a-5acf-4135-8073-a61f6bcb8cc3)
![influxsetup](https://user-images.githubusercontent.com/28630321/187088939-492e8910-395b-4aef-b1f8-199ea98a2dc8.jpg)



 

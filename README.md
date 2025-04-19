# PySpark Log File Analysis - NASA Logs Dataset


This is a simple project where I used PySpark to analyze old NASA web server logs from July and August 1995. The log files are huge, so normal tools like pandas aren't ideal - PySpark handles them easily.

The goal was to parse the raw logs and extract useful info like:

- Most visited pages
- Which IPs sent the most requests
- What times of day had the most traffic
- HTTP status code breakdown (like 404 errors, etc.)

I loaded the compressed .gz log files, used regex to split each line into fields (IP, date, request, status code, etc.), and then ran some basic analysis using Spark.

Everything runs inside a Google Colab notebook, and you just need the two log files:
1. NASA_access_log_Jul95.gz
2. NASA_access_log_Aug95.gz

You can get them using below:
- !wget ftp://ita.ee.lbl.gov/traces/NASA_access_log_Jul95.gz
- !wget ftp://ita.ee.lbl.gov/traces/NASA_access_log_Aug95.gz

No fancy visuals in this one — it's mostly about learning how to work with big log data using PySpark.
<h5 align="Left"> HTTP Status Code Visualizations</h5>

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/6de5ce62-243e-45e8-99ad-4a48d920ddcb" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/8207b466-e189-43d2-a266-d20712464213" width="300"/></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/f364b248-5044-4159-92a3-d1b2e7cd2a1a" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/71c86bba-ce7e-4e2f-b1c2-c87fece2b118" width="300"/></td>
  </tr>
</table>


Might add anomaly detection or a dashboard later. For now, it’s a solid intro to big data processing.

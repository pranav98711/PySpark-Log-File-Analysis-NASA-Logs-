# PySpark-Log-File-Analysis-NASA-Logs-


This is a simple project where I used PySpark to analyze old NASA web server logs from July and August 1995. The log files are huge, so normal tools like pandas aren't ideal — PySpark handles them easily.

The goal was to parse the raw logs and extract useful info like:

- Most visited pages
- Which IPs sent the most requests
- What times of day had the most traffic
- HTTP status code breakdown (like 404 errors, etc.)

I loaded the compressed .gz log files, used regex to split each line into fields (IP, date, request, status code, etc.), and then ran some basic analysis using Spark.

Everything runs inside a Google Colab notebook, and you just need the two log files:
1. NASA_access_log_Jul95.gz
2. NASA_access_log_Aug95.gz

You can find them here and here.

No fancy visuals in this one — it's mostly about learning how to work with big log data using PySpark.

Might add anomaly detection or a dashboard later. For now, it’s a solid intro to big data processing.

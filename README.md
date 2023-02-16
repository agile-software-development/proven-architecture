# Proven Architecture
This is a prototype code of task module of todo project.
<br>
This project implements simple version of desired logic in order to find and reduce risks.
<br>

## Results:
As you can see, provided architecture meets requirements and there is nothing to be woried about. 
```log
This is ApacheBench, Version 2.3 <$Revision: 1879490 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking localhost (be patient)
Completed 200 requests
Completed 400 requests
Completed 600 requests
Completed 800 requests
Completed 1000 requests
Completed 1200 requests
Completed 1400 requests
Completed 1600 requests
Completed 1800 requests
Completed 2000 requests
Finished 2000 requests


Server Software:        nginx/1.23.3
Server Hostname:        localhost
Server Port:            8000

Document Path:          /back/task/
Document Length:        28 bytes

Concurrency Level:      10
Time taken for tests:   5.898 seconds
Complete requests:      2000
Failed requests:        1993
   (Connect: 0, Receive: 0, Length: 1993, Exceptions: 0)
Total transferred:      732899 bytes
Total body sent:        406000
HTML transferred:       60899 bytes
Requests per second:    339.12 [#/sec] (mean)
Time per request:       29.488 [ms] (mean)
Time per request:       2.949 [ms] (mean, across all concurrent requests)
Transfer rate:          121.36 [Kbytes/sec] received
                        67.23 kb/s sent
                        188.59 kb/s total

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.0      0       0
Processing:    14   29   5.7     29      70
Waiting:       14   29   5.7     29      70
Total:         15   29   5.7     29      70

Percentage of the requests served within a certain time (ms)
  50%     29
  66%     31
  75%     32
  80%     33
  90%     36
  95%     39
  98%     43
  99%     45
 100%     70 (longest request)
```
## Setup:
```bash
docker-compose up
```
## Run loadtest:
```bash
ab -p post_data.json -T application/json -H 'Content-Type: application/json' -c 10 -n 2000 http://localhost:8000/back/task/
```

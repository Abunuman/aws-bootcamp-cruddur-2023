# Week 2 — Distributed Tracing

## Technical Tasks
---
- [X] TASK 1

* Instrument our backend flask application to use Open Telemetry (OTEL) with Honeycomb.io as the provider.

Opentelementry in the Requirement.txt

![Alt text](../images/requirement.txt-open-telemetry.png)

Honeycomb Provider 
![Opentelemetry](../images/Honeycomb-opentelemetry.png)

![app.py Config](../images/app.py-Honeycomb.png)

![Other Configurations in app.py](../images/app.py-Honeycomb.png)

* Run queries to explore traces within Honeycomb.io

Here are the results of the trace queries:

![Querry 1 - Taces](../images/Honeycmb-querry.png)

![Querry 2 - percentile](../images/Honey-querry2.png)

While running the home-activities logger querry, an error data occured 

![Error Querry](../images/Honeycomb-querry.png)

After hours of debugging, it was found out to be a boolean written instead of a string data in the config file.
And this was corrected as seen in the picture below

![Boolean/String error position](../images/Boolean-error.png)




- [X] TASK 2

* Instrument AWS X-Ray into backend flask application.

![Config 1](../images/Xray-config2.png)

![Config 2 provider](../images/X-rayapp.py.png)

![Config ](../images/Logger2-Xray.png)

* Configure and provision X-Ray daemon within docker-compose and send data back to X-Ray API.

![X-ray Daemon](../images/Xray-Daemon.png)

![X-ray Daemon Console](../images/X-rayDaemon-console.png)

* Observe X-Ray traces within the AWS Console
It came back with some traces


After this task, I ran out of Gitpod Credit and had to set up a Codespace 
 I set it following the instructions. Here is a snippet of that:

 ![Codespaces](../images/Codespaces.png)

Integrate Rollbar for Error Logging

![Rollbar Conig](../images/Rollbar-config-2.png)

![Rollbar](../images/app.py-rollbar.png)

Query received listening on Flask app

![Alt text](../images/Occurences-Rollbar.png)

![Alt text](../images/Rollbar-Occurences-dashboard.png)


Install WatchTower and write a custom logger to send application log data to CloudWatch Log group

Watchtower

![Alt text](../images/requirement.txt-open-telemetry.png)

`pip install -r requirements.txt`

Custom Logger

![Logger Config](../images/Logger-Config-Cloudwatch.png)

![Log Group crudur](../images/Loggroups.png)

![Log Streams](../images/Loggroups-Cloudwatch.png)

## Homework Challenge
---

Add custom instrumentation to Rollbar to add more attributes, userid etc

![Alt text](../images/Person-Tracking-app.py.png)

![Alt text](../images/Person-Tracking-Rollbar.png)

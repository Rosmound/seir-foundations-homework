Rosmound's Homework Notes Regarding Slack and Balerica-AI Agents integration.

(hw1_hello_slack.py )Homework 1 taught me how to send a Slack alert from a Python script using a function call.
- send_alert(...) passed the alert details—agent name, severity, message, and incident ID—to the shared Slack helper.
- f"Hello from {MY_NAME}..." used an f-string to insert your name into the message.
- The delivered check showed whether the alert was sent or skipped.
You confirmed it worked when the “Hello from RosBailey!” message appeared in #balerica-alerts.

What Script 2/Homework 2 taught me 								hw2_severity_tour.py (Severity tour & threshold filtering)


Severity is how serious an alert is:
- INFO: an ordinary update
- WARNING: something may need attention
- ERROR: something failed
- CRITICAL: an urgent or severe problem

SLACK_ALERT_SEVERITY sets the lowest severity Slack should receive. It isn’t an “only send this exact level” setting:

Threshold in .env	Alerts that pass
INFO;		INFO, WARNING, ERROR, CRITICAL
WARNING;	WARNING, ERROR, CRITICAL
ERROR;		ERROR, CRITICAL
CRITICAL; 	CRITICAL

For Script 3/Homework 3					hw3_server_time.py (UTC timestamp & clock offset analysis)


The message printed was "Message: Time check from EC2: it is Friday November 06, 2026 at 03:13:50 UTC here. Servers speak UTC!" Which UTC matched British time. Its a global time and not synched with London however, it is used because...

                                          									(Global Time & Synchronization):

What you learn: Why cloud infrastructure relies strictly on UTC via NTP, and how timezone mismatches can break distributed applications and audit logs.
Significance: If a bank transaction happens in Virginia, London, and Tokyo, everyone needs to agree on the exact microsecond it occurred. UTC synchronization prevents catastrophic data corruption in financial databases.


For Script 4/Homework 4 								hw4_disk_watch.py

The alert message did also ask "Why is a quiet INFO alert here good design, rather than a failure?"


The alert message printed was "Disk is 25.4% used -> severity INFO." A quiet INFO status indicates that disk usage is within safe operating limits. Good monitoring design avoids spamming notification channels with constant healthy updates, which prevents alert fatigue and ensures engineers only get woken up or pay attention when actual thresholds (WARNING or ERROR) are breached.

For Script 5/Homework 5									hw5_load_check.py

What happened: Inspected the system's CPU load averages using operating system metrics and dynamically triggered an alert based on processor strain.
Why it matters: High CPU load averages indicate that tasks are queuing up faster than the processor can handle them. Monitoring load helps catch runaway processes, traffic spikes, or infinite loops before the web server freezes up entirely.

The message printed was Message: Load average: 0.07 (1m), 0.02 (5m), 0.00 (15m) on 2 CPU(s).

The Question: What would make this number spike on the Balerica bank?
The Answer: On a banking application like Balerica Bank, CPU load averages (like the 0.07 shown in your terminal) would spike due to heavy computational operations, such as:
Massive API Traffic Spikes: A sudden rush of clients querying account balances or executing transactions simultaneously.
Heavy Database/Ledger Queries: Running complex, unindexed searches through large financial transaction ledgers.
COBOL Subroutine Processing: Compiling or executing intensive COBOL backend binaries on demand.
Runaway Processes or Infinite Loops: A bug in the FastAPI application code causing a CPU core to pin at 100% utilization.



For Script 6/Homework 6									hw6_incident_drill.py

The script ran a fake alert to showcase what happens when alerts are triggered during 3am. It then asked us a question(Below) to which the answer is obviously "CRITICAL" not "WARNING" or "ERROR"

The Question: Which of these fake incidents deserves to wake a human at 3 AM?
The Answer: Only CRITICAL severity incidents (such as complete database outages, ledger corruption, or payment gateway failures) deserve to wake an engineer at 3 AM. A WARNING like a batch job running slightly longer should not page someone in the middle of the night—it should create a ticket for the morning team to review, protecting engineers from alert fatigue.

For Script 7/Homework 7									hw7_morning_report.p

What happened: Executed the capstone morning report script (hw7_morning_report.py), which successfully compiled multiple system metrics (current UTC timestamp, host metadata, Python version, root disk usage percentage, and 1-minute CPU load) into a single, clean multi-line status report delivered straight to Slack.
Why it matters: In production operations, automated morning reports give engineers an instant, high-level overview of system health right at the start of the day without requiring them to manually run checks across multiple tools or servers.



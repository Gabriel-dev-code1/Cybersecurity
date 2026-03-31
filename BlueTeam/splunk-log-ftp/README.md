
#OBJECTIVE#

Perform the ingestion and analysis of FTP logs using Splunk to identify access patterns and possible anomalies.

#Logs#
The file was manually uploaded to Splunk and analyzed via SPL searches. The created file was fictitious, containing users who do not exist and simulating actions such as login and file manipulation.

#Analysis#

to view the logs, was used:
index=ftp and
sourcetype=ftp.logs

#Evidences#

-File upload-

-All events-

-Event count by user-

-Events envolving: file "uploads"-

-Events envolving: action "login failed"-

-Events envolving: action "delete"-

-Events envolving: action "download"-



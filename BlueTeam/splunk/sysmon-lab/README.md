# Splunk Sysmon Detection Lab

This project demonstrates the configuration of Splunk Free with Sysmon for the detection of suspicious processes.

## Technologies

- Splunk Free
- Sysmon
- Windows Event Logs

## Created Detections

- PowerShell execution
- creation of suspicious processes
- CommandLine monitoration

## Query example

index=sysmon
| rex field=_raw "<Data Name=\"Image\">.*\\\\(?<ProcessName>[^\\\\]+\\.exe)</Data>"
| rex field=_raw "<Data Name=\"User\">(?<User>[^<]+)</Data>"
| table _time ProcessName User
| sort -_time

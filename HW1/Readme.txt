Interpretation for the ER diagram

RELATIONS - 

EMPLOYEE - HEALTH REPORT APP
Every employee will mandatorily register on the app & the app will have multiple employees
EMPLOYEE - TEMPERATURE SCAN
One employee can have multiple temp scans & each temp scan will be associated with one employee
TEMPERATURE SCAN - COVID TEST
Each scan may lead to an on-site test & each test was performed after a scan
HEALTH REPORT APP - SELF REPORTING
Any employee may self-report & every self-report is associated with an employee
SELF REPORTING - COVID TEST
Every reported case will be required to take a test & every test is associated with a self-reported case
COVID TEST - LOCATION
Every test is associated with a location & every location is associated with a test
COVID TEST - HEALTH REPORT APP
Every test result has to be reported on the health app & health app may have a test result associated with it
HEALTH REPORT APP - CONTACT TRACING
All positive tested employees can be traced in contact tracing & each entry in contact tracing is a positive tested employee
CONTACT TRACING - MEETING
Contact tracing contains meeting locations & some meeting locations may be associated with contact tracing
All meeting rooms have a floor associated with them & vice versa
MEETING - MEETINGS_ATTENDED 
All meeting attendees are associated with multiple meetings & vice versa
MEETINGS_ATTENDED - NOTIFICATION
All attendees are alerted and alerts are sent to meeting attendees only
NOTIFICATION- HEALTH REPORT APP
Health app may receive 0 or many alerts & all alerts are sent to the health app
HEALTH REPORT APP - QUARANTINE
Some positive tested employees are required to quarantine & update daily & are all quarantine employees were tested positive
HEALTH REPORT APP - HOSPITALIZED
Some positive tested employees are required to hospitalised & updated daily & are all hospitalised employees were tested positive
CONTACT TRACING - FLOOR
All employees of a particular floor are traced & vice versa
CONTACT TRACING - NOTIFICATION
All employees on the infected floor are notified & notifications are only sent to employees on that particular floor

ENTITIES - 

EMPLOYEE
Mandatorily enrolls on HEALTH REPORT APP 
Randomly gets selected for TEMPERATURE SCAN 
HEALTH REPORT APP 
Receives current status of employee from QUARANTINE
Receives current status of employee from HOSPITALIZED
Receives covid test report of employee from COVID TEST
Receives employee self reports from SELF REPORTING
Receives alerts/notifications from NOTIFICATIONS 
TEMPERATURE SCAN 
Employees with high temperature/ with no symptoms are sent for mandatory covid test
COVID TEST
Employee can choose location where they can get tested
Temperature screening employees will see location = onsite by default
SELF REPORTING
Employees who self report their symptoms will be required to take a covid test
Employees will self report on the HEALTH REPORT APP 
CONTACT TRACING
Positive test reports will trigger CONTACT TRACING
Will trace employees in meetings with infected employee
Will trace employees on same floor as infected employee
MEETINGS ATTENDED
Has composite PK = employee_id + meeting_id
NOTIFICATION
Employees in MEETINGS ATTENDED will receive alerts
Employees in FLOOR will receive notifications
QUARANTINE
Positive tested employees are required to be quarantined
HOSPITALIZED
Positive tested employees may get hospitalized

Others - 
LOCATION 
Onsite/offsite
MEETING
Meeting room, floor, employees present, start time
FLOOR
Floor number
Building number


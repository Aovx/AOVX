**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v09
**Function & Feature Update：**
1.Modify buffer to check for failed attempts


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v08
**Function & Feature Update：**
1. Modify buffer write failed
2. Modify the switch between workmode 2 and 4 to change the sampling and reporting time
3. Modify the tracking mode short connection OTA failed
4. Modify the problem of synchronizing time in a long-time shielded environment


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v07
**Function & Feature Update：**
1. Modify the full battery state and the voltage value does not correspond, restart or the first start-up voltage value is low
2. Add the battery percentage of A device
3. Modify the reading value of GSensor to 0, especially in the case of light triggering
4. Modify HDOP positioning failure to 0
5. Modify OTA related issues
6. Modify the text message reading


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v06
**Function & Feature Update：**
1. Modify the platform OTA failure problem
2. Modify AT commands (QWIFI, QBT, QTEMPHUMI, QADC)
3. Modify the minimum sampling and reporting time to 360s


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v05
**Function & Feature Update：**
1. Modify the maximum power value, light triggers power acquisition
2. Modify the text message reading, SMS OTA
3. The default report mask contains neighbor cell information
4. CSQ99 reacquired once


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v04
**Function & Feature Update：**
1. Failed to modify SMS OTA
2. Modify 8105 response error, OTA success did not reply


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v03
**Function & Feature Update：**
1. Optimize the battery percentage, and the battery fluctuates
2. Optimize vibration false triggering
3. Modify the situation where the base station information is obtained successfully, but the message base station is NULL
4. Modify the base station to reacquire when the distance from the last acquisition exceeds 300s
5. Add FOTA status
6. Modify the SMS to send OTA upgrade, and the command to read the SMS times out


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v02
**Function & Feature Update：**
1. Add AT to query the number of WIFI and BLE, modify the return value of the FORMAT command and delete the blind zone
2. Modify gsensor to read error value processing and vibration false triggering issues
3. Do not sleep after modifying the serial port wake-up operation
4. Modify the maximum time for reporting buffer to 9 minutes and 30 seconds, and optimize buffer for TIMEOUT
5. Modify the light trigger to affect the voltage value
6. Optimize the case where the base station information is NULL
7. When the main IP is modified and the backup error is correct, the backup buffer data will be lost
8. Optimize battery percentage
9. Modify the module OTA prompt version error


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.5_v01
**Function & Feature Update：**
1.Modify the name of the OTA version to be too long, causing the upgrade to fail


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v27
**Function & Feature Update：**
1. Change the default positioning to GPS+GLO
2. Modify the analysis error of the main cell of the base station, and add the message analysis of the adjacent cell


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v26
**Function & Feature Update：**
1. Modify periodic sampling and periodic reporting
2. Mileage is fixed at 0


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v25
**Function & Feature Update：**
1. Modify the problem that periodic sampling will not be performed when there are too many buffer data and the report exceeds 10 minutes
2. Restore factory delete buffer data



**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v24
**Function & Feature Update：**
1. Modify buffer data processing
2. MNC changed to 2 bytes


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v23
**Function & Feature Update：**
1.Modify the data length error in the buffer, resulting in a read error


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v22
**Function & Feature Update：**
1.Modify the minimum value of the G-Sensor threshold to 30, and the maximum value of the read light value to 3000


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v21
**Function & Feature Update：**
1. After modifying the server correctly, when reporting periodically, the buffer data is not reported normally
2. Modify the buffer data CRC error, the platform will not reply



**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v20
**Function & Feature Update：**
1. Add LOG to display blind area read and write offset information, light threshold limit
2. Modify the buffer header file information and blind area data processing



**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.4_v16
**Function & Feature Update：**
1. Optimize GSensor, battery power, brightness
2. Add minor version number
3. Relevant issues such as modification cycle reporting, buffer storage reading, package loss, etc.
4. When adding temperature and humidity and meeting the trigger conditions at the same time, the reported data type is temperature and humidity trigger 5
5. Modify GIT known issues


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.3_v02  （archived version）
Release Date: 
Tue Sep 13 16:34:54 2022 +0800
Function & Feature Update:
1. SMS trigger in sleep state: Only when WorkMode is 2 and SleepMode is 0, it can wake up by SMS in sleep state. When WorkMode is 4, it will not actively wake up, and can re-read unread text messages and execute them when it wakes up periodically.
2. Get neighbor cell information in LTE state.
3. After the trigger message is triggered, change the trigger report, sampling period, and mode. Restores after the duration expires.
4. Optimize the problem of abnormal temperature and humidity
5. Optimize BG95 short message abnormal problem
6. Optimize the problem that SMS index 0 is filtered under dormancy, and automatically delete the read SMS
Bug Fix List：
Add commands:
1.AT+SleepMode=mode; set two sleep modes in Traking mode; 0, low power consumption of the network module; 1, no sleep;

2.AT+TriggerMode=duration, trigger condition, reporting period, collection period, mode after triggering;
After a specific trigger message is sent, it can be set to continue with the configured reporting period, sampling period, and mode. Until the duration expires, restore the original state. The trigger message will refresh the duration.
Duration: (>0) 0 is the off function, others are the duration after departure
Trigger conditions: (0-7) 0 for all triggers,
     1: LOW_POWER,
     2: MOTION,
     3: CRASH,
     4: LIGHT,
     5: TEMP_HUMI,
     6: TEMP,
     7: HUMI,
Reporting period, sampling period: when WorkMode is 4, the minimum value is 600s; when WorkMode is 2, SleepMode is 0, the minimum value is 60; when WorkMode is 2, SleepMode is 1, the minimum value is 10;
Period after trigger: (2, 4) 2:Traking 4:P+D



**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.3_v01
Release Date: 
Tue Sep 13 16:34:54 2022 +0800
Function & Feature Update:
1.Watchdog 5 minutes early



**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.2_v04
Release Date:
Mon Aug 22 15:35:56 2022 +0800
Function & Feature Update:
1. Adjust the network receiving stack size
2. Add power boost pin


**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.2_v03
Release Date:
Mon Aug 15 09:47:16 2022 +0800
Function & Feature Update:
1. Optimize the waiting time of qiopen to be less than the waiting time of the server to avoid simultaneous timeout and lead to failure to connect successfully
2. Fix the problem that the additional GNSS positioning timestamp is not cleared
3. The CORE upgrade delay cancels the AT transmission to ensure that the upgrade response message is sent normally
4. The serial port buffer is expanded to 256 to prevent the FOTA command from sending too long and failing
5. Add lock synchronization mechanism for time synchronization
6. Fix the bug that sscanf cannot convert floating point numbers




**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.2_v02
Release Date:
Thu Aug 4 16:08:21 2022 +0800
Function & Feature Update:
1. Support transparent transmission AT
2. Cancel the management server by default
3. Cancel sleep during buffer processing
**Release Version:**
AOVX_AX300-XX_H2.0_V2.0.2_v01
Release Date:
Wed Aug 3 16:06:50 2022 +0800
Function & Feature Update:
1. Fix the problem that temperature, humidity and light can still trigger within the timeout period
2. The version number limit is changed to a minimum of 10 characters
3. 8105/8104 send data reply immediately
4. Add some debugging logs
5. Fix the occasional wrong reading of the temperature and humidity sensor
6. Adjust the buffer length of the debug serial port

**Release Version:**
AOVX_AX300-XX_H1.2_V2.0.1_v05
Release Date:
Wed Jul 27 19:32:19 2022 +0800
Function & Feature Update:
1. Fix module fail 2 problem
2. Support sharing of RI and Sensor interrupt
3. Fix the problem of buffer length -1
4. Fix the sleep bug when downloading the core version

**Release Version:**
AOVX_AX300-XX_H1.2_V2.0.1_v04     
Release Date:
Tue Jul 26 20:25:17 2022 +0800
Function & Feature Update:
1. Fix the failure of module firmware upgrade
2. Support network standard configuration
3. The light trigger interval is changed to 1 minute by default
4. APP message queue is changed to 30 by default
5. Fix COPS may cause stack overflow bug
6. Avoid frequent sending of connection requests
7. The restart of the network delivery will take effect immediately
8. Repair the problem that the last temperature and humidity trigger data is 0 after the temperature and humidity enable is turned off and then reported
9. GPS time synchronization is changed to positioning and then synchronizing
 10. There may be an abnormal RTC time flip problem in optimization
 11. Optimize the problem that the wait gps print log exceeds 180s
 12. Fix the problem that the OTA download fails and cannot enter dormancy
 13. Fix the problem that the network status is repeatedly set to cause a status error


**Release Version:**
AOVX_AX300-XX_H1.2_V2.0.1_v03   
Release Date:
Tue Jul 19 14:09:23 2022 +0800
Function & Feature Update:
1. Fix restart problem
2. Change the command restart to restart immediately


**Release Version:**
AOVX_AX300-XX_H1.2_V2.0.1_v02
Release Date:
Mon Jul 18 15:41:03 2022 +0800
Function & Feature Update:
1.Fix the problem that the ADC cannot read the voltage


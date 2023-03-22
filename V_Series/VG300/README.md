# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.8_v06
**Function & Feature Update:**
1. Modify the AT+GNSS command to AT+GNSSMODE
2. Still group packages before getting time information
3. Support AT+LOCUPDATE command (report real-time position for 0 sleep, report previous position for 1)



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.8_v05     
Release Date:
Sat Feb 22 17:26:09 2023 +0800
**Function & Feature Update:**
1. Delete the electronic fence exception code


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.8_v04
Release Date:
Date: Sat Feb 11 17:26:09 2023 +0800
**Function & Feature Update:**
 1. Optimize the default setting to GPS+GLONASS AT+GNSS=1(GPS+BD) AT+GNSS=0(GPS+GLONASS). Support MA, MB

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.8_v01
Release Date:
Sat Feb 11 17:26:09 2023 +0800
**Function & Feature Update:**
1. The default setting is GPS+GLONASS AT+GNSS=0(GPS+BD) AT+GNSS=1(GPS+GLONASS)
2. Support F9 field GNSS TIME AT+AssistMask=15
3. Support AT+BLIND=0 command
4. Can be configured without login and authentication AT+LoginMode=0 (login authentication) AT+LoginMode=1 (no login authentication required)
5.8105 OTA upgrade, 404 problem
6. Fix AT command execution disorder problem


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v27
Release Date:
Tue Aug 16 09:16:00 2022 +0800
**Function & Feature Update:**
1. Add BatMode mode: AT+BatMode
2. Add anti-frequent collision report, no repeated report within 5s
3. AT password function, AT+AtPassword
4.AT+DinTime, the duration of Din1 and Din2 can be configured


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v26
Release Date:
Fri Aug 5 13:43:27 2022 +0800
**Function & Feature Update:**
1. Optimize Jamming, command AT+Jamming=(mode,URC,period)
2. Compatible with VG200 (continuously low VCC does not affect lights and virtual ignition)
3. Optimize TOW speed to 0
4. Optimize VCC disconnection report



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v25
Release Date:
Date: Thu Aug 4 09:26:39 2022 +0800
**Function & Feature Update:**
1.Add DIN1, pull DIN2 low for 1s to trigger reporting

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v24
Release Date:
Wed Aug 3 17:46:50 2022 +0800
**Function & Feature Update:**
1. Optimize the collision threshold range, 0 is to disable collision detection
2. Trailer speed is not cleared



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v23
Release Date:
Tue Aug 2 15:51:23 2022 +0800
**Function & Feature Update:**
1. Optimize ACC and VCC, connect and disconnect trigger report
2. Optimize the start trigger reporting time
3. Modify the collision trigger threshold setting range (0-255)






# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v22
Release Date:
Mon Aug 1 09:11:40 2022 +0800
**Function & Feature Update:**
1. Optimize ACC cycle ignition problem


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v21
Release Date:
Mon Aug 1 09:11:40 2022 +0800
**Function & Feature Update:**
1.Optimize ACC connection disconnection status check


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v20

Release Date:
Tue Jul 26 11:56:21 2022 +0800
**Function & Feature Update:**
1. In Gsensor virtual ignition mode, restart with ACC OFF, it is RUN, and then wait for Gsensor virtual shutdown
2. Repair and unplug the VCC, there will be two VCC disconnection messages
3. GPS time logic restoration
4. Repair the GTGEO instruction data that may fail if it is too long
5. Repair configuration latitude and longitude, the data is not allowed
6. Repair VCC connection without message, no message when connected with ACC at the same time. When connected to VCC alone, it becomes RUN
7. Optimize the serial port to read AT commands


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v19
Release Date:
Tue Jul 26 11:56:21 2022 +0800
**Function & Feature Update:**
1.Optimize the power light logic during sleep

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v18
Release Date:
Mon Jul 25 19:02:29 2022 +0800
**Function & Feature Update:**
1. Optimize the self-extinguishing of the electronic fence
2. When in deep sleep, the power light will only flash once when sending a packet


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v17
Release Date:
Fri Jul 22 16:21:32 2022 +0800
**Function & Feature Update:**
1.Optimize voltage virtual ignition



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v16
Release Date:
Fri Jul 22 12:03:52 2022 +0800
**Function & Feature Update:**
1. Optimized latitude and longitude configuration is not accurate
2. Keep latitude and longitude after self-extinguishing
3. Optimize voltage virtual flameout
4. When sleeping, send a report and turn on the power light



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v15

Release Date:
Thu Jul 21 16:58:02 2022 +0800
**Function & Feature Update:**
1.Optimize the latitude and longitude configuration


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v14
Release Date:
Thu Jul 21 11:48:48 2022 +0800
**Function & Feature Update:**
1.Optimization of the self-extinguishing state of the electronic fence



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v13
Release Date:
Wed Jul 20 19:37:50 2022 +0800
**Function & Feature Update:**
1. Optimize the latitude and longitude configuration format and time format
2. Optimize the configuration to clear the latitude and longitude

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v12
Release Date:
Wed Jul 20 15:13:15 2022 +0800
**Function & Feature Update:**
Optimize the polygonal electronic fence


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v11
Release Date:
Wed Jul 20 14:04:36 2022 +0800
**Function & Feature Update:**
1. Clear the entry and exit timing points when instructing GTGEO configuration
2. Optimize the first trigger report



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v10
Release Date:
Tue Jul 19 19:40:54 2022 +0800
**Function & Feature Update:**
1. Save the file when instructing GTGEO configuration
2. Optimize the polygon electronic fence logic



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v09

Release Date:
Mon Jul 18 14:11:06 2022 +0800
**Function & Feature Update:**
1. Optimize the electronic fence parameter file
2. Optimize voltage virtual ignition
3. Add command GTGEO
4. Optimize the electronic fence function



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v07
Release Date:
Mon Jul 18 14:11:06 2022 +0800
**Function & Feature Update:**
1. Delete the electronic fence parameter file, no need to restart. 1, 2, 3, and 4 will all be deleted, and 4 will only delete the electronic fence parameters
2. Fix the problem of failure when Mode and Trigger Mode are 2
3. GEO parameters will not be lost after power failure
4. Multilateral electronic fence


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v06
Release Date:
Wed Jul 13 19:09:03 2022 +0800
**Function & Feature Update:**
1. When TriggerMode is equal to 0, the single area function will not be executed when the latitude and longitude is 0. When TriggerMode is not equal to 0, it does not judge that the latitude and longitude are 0
2. Optimize VCC and ACC connection reporting
3.format=5, delete the electronic fence file


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.7_v05
Release Date:
Tue Jul 12 18:13:59 2022 +0800
**Function & Feature Update:**
1. Add the command SensorMask
2. Optimize VCC connection reporting
3. Relaymode command configuration, factory test
4. Virtual ignition mode. AT+VirtualMode. 0, vibration virtual ignition, 1, voltage virtual ignition
5. Geo-fence (circular), the data is in GEOFENCE_INFO_FILE. Four related commands for geofence: GEOFENCEMODE, GEOFENCEPOINT, GEOFENCETIME, QGEOFENCE
6. File reading and writing plus packet processing, a maximum of 1024 bytes per packet.
7. Expand AOVX_SEND_BUF_MAX_LEN, 512 to 1024
8. Fix the failure to send the Distance command



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v11
Release Date:
Fri Jul 1 16:56:28 2022 +0800
**Function & Feature Update:**
1.Optimize the QINFO instruction



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v10
Release Date:
Fri Jul 1 16:56:28 2022 +0800
**Function & Feature Update:**
1. Dormant packet loss problem
2. The first positioning without latitude and longitude
3. Add SensorMask command
4. Optimize configuration printing exception
5. Two minutes short of sleep

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v09
Release Date:
Thu Jun 30 18:02:49 2022 +0800
**Function & Feature Update:**
1. The first GPS positioning has no latitude and longitude
2. Multiple reports for the first positioning
3.DeepSleep timeout processing



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v08
Release Date:
Thu Jun 30 15:06:35 2022 +0800
**Function & Feature Update:**
1. Remove the operation of reading backup data;
2. Report startup package optimization;
3. Optimize to sleep only after receiving the response from the main server


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v07
Release Date:
Thu Jun 30 09:18:10 2022 +0800
**Function & Feature Update:**
Modify the infinite restart problem of the new version 1.2.3.

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v06
Release Date:
Tue Jun 28 10:22:57 2022 +0800
**Function & Feature Update:**
1. Cancel DeepSleep, turn off GNSS and cancel the first positioning report packet, and exit only after sending a periodic report packet;
2. Optimize the boot package report;
3. Status light optimization


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v05
Release Date:
Tue Jun 28 10:22:57 2022 +0800
**Function & Feature Update:**
1. Optimize the OTA failure package to report multiple times
2. Optimize power failure and power supply without OTA successful report


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v04
Release Date:
Mon Jun 27 09:44:10 2022 +0800
**Function & Feature Update:**
1.2G Deep sleep mode. Command AT+DeepSleepMode=1 (default 0, off. 1 on)



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v03
Release Date:
Thu Jun 23 11:44:36 2022 +0800
**Function & Feature Update:**
1. Charging start and full trigger reporting (charging and discharging lasts for 15s to be valid)
2. OTA start, success, failure trigger reporting

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v02
Release Date:
Tue Jun 21 18:11:35 2022 +0800
**Function & Feature Update:**
1. Charging start and full trigger report (charge and discharge lasts for 5s to be valid)
2. Add AT to close oil circuit limit (speed limit)
3. The sensor is enabled by default


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.6_v01
Release Date:
Thu Jun 16 13:55:19 2022 +0800
**Function & Feature Update:**
1. Charging start and full trigger report
2. Soft reset trigger report
3. When the speed is higher than 20km/h, the oil-off state will not be executed


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v07
Release Date:
Tue Jun 14 15:17:46 2022 +0800
**Function & Feature Update:**
1. Modification: low voltage will cause voltage virtual flameout
2. Improve GNSS auxiliary functions


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v06
Release Date:
Mon Jun 13 19:52:11 2022 +0800
**Function & Feature Update:**
1. Distance trigger reporting;
2. Repair the effective vibration duration function


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v05
Release Date:
Mon Jun 13 15:28:25 2022 +0800
**Function & Feature Update:**
1. The trailer status ACC is off;
2. Repair the failure of setting the driving, parking, and sleeping parameters issued by the platform


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v04
Release Date:
Fri Jun 10 17:02:16 2022 +0800
**Function & Feature Update:**
1. Trailer status ACC is off
2. Continuous no vibration duration, default 300
3. AT+Shakerange command return value
4. Repair the failure of the platform to send driving, parking, and sleep parameter settings
5. Cancel sleep and repeat report



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v03
Release Date:
Fri Jun 10 13:54:43 2022 +0800
**Function & Feature Update:**
1. AT+GnssAst? Default 0
2. Trailer status, ACC ON, unable to enter driving mode: connect to immediately exit TOW, report tow exit and acc ignition
3. Modify the trailer state oil circuit is always open
4. After AT+FUEL=off, the status in the message and the oil circuit status bit in the GPIO module are 1
5. Modify trailer status, ACC ON TIME will not accumulate
6. It is recommended to enter sleep mode 1 minute after exiting trailer mode
7. Issue AT+FUEL=ON, what is issued and what will be returned
8. Modify the status of exiting the trailer, and report the trailer stop alarm
9. It is recommended that when the trailer is in the state, the ACC state flag is off
10. After the ACC is OFF, in the parking state, shaking the device, it cannot enter the sleep mode
11. Fix the problem that the Shakerange command cannot reset Sc7a20e
12. Add ShakeTime, Shake, Shakerange, Crashrange command functions
AT+Shakerange=1, 2, 3 (the first digit is meaningless, the second digit: vibration positive and negative range 0:2g 1:4g 2:8g 3:16g, the third digit: vibration sensitivity 0-255)
AT+Shake=0,3,0 (the second digit is effective, representing the effective duration of shaking)
at+Crashrange=460 (collision threshold level)
AT+ShakeTime=3,500 (judging the effective shaking time, judging the non-shaking time)



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.5 v02
Release Date:
Tue Jun 7 18:55:04 2022 +0800
**Function & Feature Update:**
1. GNSS switch control (GPIO_0)
2. Voltage compensation (+500)
3.APN three are all empty
4. GPS time synchronization problem
5. Repair the parking state vibration will reset the sleep timer
6. Abnormal burning of blank device



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.4 v03
Release Date:
Tue Jun 7 18:55:04 2022 +0800
**Function & Feature Update:**
1. G-sensor virtual ignition, trigger ignition + flameout report. Change the G-sensor driver to trigger vibration detection through interrupts
2.G-sensor+GNSS assisted positioning virtual ignition, trigger ignition report. Add AT command to control GNSS auxiliary switch, AT+GnssAst
3. Tow mode trigger reporting (start and end)
4. To report the distance, add AT command to configure the distance report value, AT+Distance
5. Collision trigger report
6. Relay output status bit, Tow mode status bit, abnormal displacement status bit
7. The platform controls the factory settings, and the mileage is cleared
8. Repair three voltage values (driving, sleep, parking) failed to modify
9. Abnormal situation: AT+FUEL=ON, the return is the real state of the current oil circuit. Solution: AT+FUEL can check the current status and the value to be set
10. When AT+FUEL=OFF is issued, no switching will be performed 5 times when it is currently OFF
11. Repair the AT+FUEL/command, the device will restart abnormally
12. The AOVX prefix of the version number supports customization, AT+COMPANY=AOVX
13. Convenient on-site measurement and statistics, the IMEI printing position is moved forward;
14.qinfo, net data and network status are consistent
15. Repair issued AT+FORMAT=2, Accontime value is not cleared
16. After repairing FOTA upgrade restart, the AccOnTime time is smaller than the time before the upgrade


# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.4 v02
Release Date:
Fri May 27 12:44:21 2022 +0800
**Function & Feature Update:**
1. Add switching TCP/UDP mode, only for server 1 and 2: TCP: AT+ReportMode=0 UDP: AT+ReportMode=1
2. Fix AT+FORMAT=2, Accontime value is not cleared
3. After repairing the OTA upgrade restart, the AccOnTime time is smaller than the time before the upgrade
4. Fix UnKnowID bug



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.4 v01
Release Date:
Tue May 24 16:55:34 2022 +0800
**Function & Feature Update:**
1. When the authentication password is not a string, the reading length is abnormal bug
2. QINFO instruction to add NET information
3. Overspeed continuous reporting of bug fixes
4. Optimize the BUG caused by the inconsistent length of the initialization read file
5. Fix the bug that SMS FOTA upgrade does not reply to SMS and replying to SMS will cause FOTA upgrade to fail
6. GNSS AT command optimization, GPS changed to GNSS
7. ACC ON TIME is the total time of ACC
8. The default time zone is 0
9. Oil-on command, 0 is changed to open oil, 31 is changed to cut-off oil
10. GPS commands support latitude and longitude
11.33% Brick when power off during upgrade. It can be solved with firmware version 08.

# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.3 v05
Release Date:
Wed May 11 10:35:40 2022 +0800
**Function & Feature Update:**
Fix the problem that processing seq in 808 may cause negative values



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.3 v04
Release Date:
Mon May 9 11:42:09 2022 +0800
**Function & Feature Update:**
1. Support oil circuit logic, change oil to fuel, support case
2. Support gpiovaule command
3.AT command supports spaces



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.3 v03
Release Date:
Fri May 6 16:10:28 2022 +0800
**Function & Feature Update:**
1. Fix 808 protocol OTA upgrade failure problem --- FOTA upgrade driving mode and sleep mode --PASS
2. Support Sensor and auxiliary information mask configuration and reporting





# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.3 v02
Release Date:
Thu Apr 28 10:13:10 2022 +0800
**Function & Feature Update:**
1. The sending queue is full and the blind area is directly stored
2. If the sending interval is lower than the timeout interval, no reply will be detected




# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.3 v01
Release Date:
Wed Apr 27 21:46:46 2022 +0800
**Function & Feature Update:**
1. Support 808 downlink parameter configuration/control and reply configuration
2. Optimization of sending and receiving data seq confirmation process
3. Fix the 808 underlying protocol length overflow bug
4. Change the sending buffer to queue mode



# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.2 v01
Release Date:
Wed Apr 20 17:28:21 2022 +0800
**Function & Feature Update:**
1. Fix the occasional failure to execute AT commands after waking up from sleep
2. Optimize the network process
3. Fix the bug that the roaming network may not be able to log in to the network
4. Because AGPS's overseas network may affect data services, it is temporarily canceled
# Release Version:
AOVX_VG300-GL_H1.2_MC25MAR01A07_V1.2.1 v01
Release Date:
 Fri Apr 1 19:48:48 2022 +0800
**Function & Feature Update:**
1. Support reporting mask, by default only report mileage, main base station and power supply voltage


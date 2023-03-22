**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v06
**Function & Feature Update:**
1. Modify the problem that GPS is turned off when deep sleep LOCUPDATE=2

**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v05
**Function & Feature Update:**
1. Increase the global variable array storing seq to 200 seq records for each server
2. During the sleep countdown, the trailer still enters sleep after being triggered


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v04
**Function & Feature Update:**
1. In the AT+QISEND=0,0 process, compare the seq of the currently sent data packet with the latest seq in the global structure array every second. If they are equal, it means that the data has been successfully sent. At this point, end AT+QISEND= 0,0 process
   Applicable to the real result that the server reply may be faster than AT+QISEND=0,0 in a weak network environment, improve software efficiency and reduce the generation of duplicate blind area data. *
   Modify the AT+QISEND=0,0 process to be every second, up to five seconds;
2. The software reset will no longer reset the packet serial number


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v03
**Function & Feature Update:**
1. Add AT+DO1MODE command, the default is equal to 0, when it is equal to 1, it is used for DVL; DO1 outputs high level when overspeed*


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v02
**Function & Feature Update:**
1. Add a global structure array to save the 0x0200 serial number in the received two server 0x8001 data packets. When sending blind area data, it will compare the seq of the packet data with the seq in the saved array. If The same means data duplication;
Discard the data in the blind area of the packet*


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.5_v01
**Function & Feature Update:**
1. Modification of version number
2. Modify the readback problem of the LOCUPDATE command


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v09
**Function & Feature Update:**
1. When the counter triggered by DI1 is directly powered off, the count will not be lost
2. Modify the logic after the data packet QISEND, with the reporting interval set at 15 seconds. When the reporting interval is greater than or equal to 15 seconds, the judgment is based on waiting for the server to reply, and the maximum waiting time is 15 seconds; when the reporting interval is less than 15 seconds, the result of AT+QISEND=0,0 is used as the basis. The two mechanisms are only applicable to data on the master server.
3. Modify the speed threshold value when the oil circuit is turned off to 30km/h. If the vehicle speed is greater than 30km/h when the oil circuit is turned off, it will not be able to close the oil circuit when the speed drops to meet the conditions and then it will be automatically closed.


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v08
**Function & Feature Update:**
1. The 0XF9 auxiliary information field increases the counter triggered by DI1, and the count is continuously accumulated for each trigger and the restart will not reset the number of times. AT+ASSISTMASK=16 enables this report
   In addition, add AT+DI1CNT command to query and configure the counter (required by ECOFOR on the evening of 3.6)


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v07
**Function & Feature Update:**
SLEEPMODE:0 LOCUPDATE:0 Keep GPS on for the first two hours after entering light sleep, then turn on GPS every time you report, and turn off GPS after the package is completed
SLEEPMODE:0 LOCUPDATE:1 Keep GPS on for the first two hours after entering light sleep, then keep GPS off until the vehicle is turned on
SLEEPMODE:0 LOCUPDATE:2 When the device enters sleep mode, the GPS will not be turned off, and the previous position will be reported
SLEEPMODE:1 LOCUPDATE:0 Turn off GPS after entering deep sleep, then turn on GPS every time you report, turn off GPS after the package is completed
SLEEPMODE:1 LOCUPDATE:1 Turn off GPS after entering deep sleep, then keep GPS off until the vehicle is turned on
SLEEPMODE:1 LOCUPDATE:2 The device will not turn off GPS when it enters sleep mode, and report the previous position


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v06
**Function & Feature Update:**
1. Modify the GPS positioning flag BIT1 in the protocol status field. As long as the reported latitude and longitude is not empty, it will report 1, otherwise it will be 0; add BIT26 as the original function (internal use, not open to customers)
2. The previous version used GPS+BD by default, but now it is changed to GPS+GLO by default, but it cannot be modified automatically for old devices, so it is forced to set after booting and update the configuration in flash


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v05
**Function & Feature Update:**
1. Modify the problem that the mileage in the first two packets of data after restarting is 0
2. The position is not updated when the vehicle ACC is turned on but not driving*
3. Add trigger, AT command report AT+ATREPORT


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v04
**Function & Feature Update:**
1. Light sleep system light problem modification
2. Modify the logic of GPS on and off in light sleep and deep sleep
Bug Fix List
SLEEPMODE:0 LOCUPDATE:0 Keep GPS on for the first two hours after entering light sleep, then turn on GPS every time you report, and turn off GPS after the package is completed
SLEEPMODE:0 LOCUPDATE:1 Keep GPS on for the first two hours after entering light sleep, then keep GPS off until the vehicle is turned on
SLEEPMODE:1 LOCUPDATE:0 Turn off GPS after entering deep sleep, then turn on GPS every time you report, turn off GPS after the package is completed
SLEEPMODE:1 LOCUPDATE:1 Turn off GPS after entering deep sleep, then keep GPS off until the vehicle is turned on




**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v03
**Function & Feature Update:**
1. Fix the problem that the ID in the message is 0 after booting
2. When LOCUPDATE is 1, the GPS is not turned on, and when it is 0, the GPS is turned on and the GPS is turned off after the packet is assembled.
3. Fix the problem of false reporting of inflection points during sleep
4. Fix the problem that the number of satellites is 0, but the positioning is yes, and the latitude and longitude are also updated
5. Fix the problem that the deep sleep cycle wakes up without grouping and reporting


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v02
**Function & Feature Update:**
1. The base station positioning is not reported by default (it will not be reported if the mask is configured)


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.4_v01
**Function & Feature Update:**
1. Base station information MNC modification
2. The soft reset repeatedly sends the restart package problem


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v18
**Function & Feature Update:**
1. Optimize the problem of data loss in buffer
2. The minor version number of the software is increased



**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v17
**Function & Feature Update:**
1. Repair the blind area data loss caused by module error code 402 and 412, hang test search log ERROR|>>>RecoverBuffer



**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v16
**Function & Feature Update:**
1.at+locupdate=1, turn off GPS regularly after light sleep


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v15
Function & Feature Update:
1. Turn off the cold start soft reset function of the GPS module


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v14
**Function & Feature Update:**
1. JAMMING related AT command added


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v13
**Function & Feature Update:**
1. Unable to locate for three minutes, GPS power off and on again, still unable to locate after two minutes GPS module cold start soft reset
2. Store the EXTRA queue data in the blind area before the device restarts
3. Repair the data loss of the EXTRA queue caused by the state error of the deep sleep wake-up module

**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v12
**Function & Feature Update:**
1. Light sleep can also send buffer data

**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v11
**Function & Feature Update:**
1. Increase the length of the memory queue for saving data when the save module restarts
2. Add NOJAMMING trigger


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v10
**Function & Feature Update:**
1. Correction of false positives at inflection point
2. Vehicle idling flag increased
3. Add 10s when saving the local time before restarting
4. Modify the module to restart and lose data
5. Reduce local time error


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v09
**Function & Feature Update:**
1. Modify the inflection point problem
2. Buffer reading optimization
3. Modify the module to lose data when restarting


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v08
**Function & Feature Update:**
1. Optimization of inflection point leakage triggering problem
2. Save the current system time in flash before each restart, and read it after restarting, so as to avoid not getting the time when there is no network and cannot locate


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v07
**Function & Feature Update:**
1. The wake-up package condition of the deep sleep cycle is increased. After the positioning is successful or 40S after wake-up, the package data is sent directly to sleep


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v06
**Function & Feature Update:**
1. Modify the processing of inflection point data
2. When the QHTTPGET command does not get a reply, it is determined that the OTA has failed


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v05
**Function & Feature Update:**
1. Optimize buffer reading and writing
2. Add the AT+LOCUPDATE command, when it is 0, it will sleep and report the real-time position, and if it is 1, it will report the position before
3. Delete AT+OPENGPSTM command
4. After the device is powered on or restarted, if the module type is not obtained, change the device name to Vx300 (previously VM300_GL)


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v04
**Function & Feature Update:**
1. Fix DI1_UP false alarm problem
2. Make the factory test AT+QWIFI pass normally
3. Inflection point data loss increases debug log
4. Inflection point false negative optimization
5.VM300 also uses AT+QISEND=0,0 mechanism
6. Fix the data loss in the blind area caused by restarting without network equipment for a long time


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v03
**Function & Feature Update:**
1. Fix the problem of acceleration misfire


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v02
**Function & Feature Update:**
1. Fix the problem that GnssAge is not allowed
2. Fix the problem that it takes a long time to enter hibernation

**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.3_v01
**Function & Feature Update:**
1. Fix the problem that the company name is empty after the version upgrade
2. Do not wait for the server to reply after the data packet is sent


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v14
**Function & Feature Update:**
1. By default, 4G turns off VOLTE
AT+QIMS="disable"
2. Fix the company name query problem
3. Gnss positioning galaxy is changed to GPS+GLO by default


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v13
**Function & Feature Update:**
1. Add AT+FWNAME, you can modify the company name
2. The GPS light does not turn on when the deep sleep cycle reports the sleep


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v12
**Function & Feature Update:**
1. In three-wire mode, it cannot be woken up by acceleration during sleep


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v11
**Function & Feature Update:**
1. Repair and upgrade failure cannot enter hibernation and restart


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v10
**Function & Feature Update:**
1. Increase the GPS speed as the basis for equipment driving --> parking
2. Sleep does not turn off GPS
3. Add acceleration change as the basis for judging equipment parking --> driving


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v09
**Function & Feature Update:**
1. Fix the problem that the occasional startup package is not reported
2. After the repair tool issued the AT command to set the parameters of the electronic fence, the device was powered off and the setting data was lost
3. Fix the problem that when the deep sleep cycle is reported, the green light will be on after connecting to the server
4. Fix the error url fota upgrade command issued locally, the download fails, and the OTA failure message is not triggered


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v08
**Function & Feature Update:**
1. Modify the problem that the serial number of the log is not equal to the serial number of the message


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v07
**Function & Feature Update:**
1. HDOP outlier avoidance, set to 0 when exceeding the range


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v06
**Function & Feature Update:**
1. Add gnsstime report to F9 field
2. Fix the problem of repeated reporting of messages
3. Fix the problem that the queue data is not reported


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v05
**Function & Feature Update:**
1. Fix the system crash problem caused by thread infinite loop
2. Fix the printing problem of data package type when grouping packages
3. Delete the log to print: AngSpeed1:, AngSpeed2:, AngSpeed3:


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v04
**Function & Feature Update:**
1. Fix the problem that the speed value is abnormally large due to array out-of-bounds reading
2. When the time is not synchronized, the package is still grouped
3. Fix the problem of packet loss at the inflection point when the inflection point is triggered frequently
4. Fix the problem that SPEED_DOWN and SPEED_TURN are triggered together in log printing


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v03
**Function & Feature Update:**
1. Repair the log printing, when the sharp deceleration is triggered, the keyword of sharp turn will be added
2. Fix the speed value error caused by uninitialized global variables
3. The trigger condition of rapid acceleration and rapid deceleration is changed to 8km/h


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v02
**Function & Feature Update:**
1. The AGPS function needs to be verified, and the master branch should be closed first.
2. Support DI1 and DI1_UP trigger to wake up sleeping devices and report messages


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.2_v01
**Function & Feature Update:**
1. Turn on the AGPS function
2. Add rapid acceleration, rapid deceleration, sharp turn detection
3. DI1 supports double edge interrupt


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v08
**Function & Feature Update:**
1. Repair sending "AT+btmode=31,0" AT command, the device data is out of bounds and hangs
2. After repairing "AT+BTENABLE=0", the device is still scanning Bluetooth information from the LOG, and the Bluetooth information will also be reported in the message


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v07
**Function & Feature Update:**
1. Fix the bug in the parameter area after the upgrade


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v06
**Function & Feature Update:**
1. Modify the URC processing thread stack space

**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v05
**Function & Feature Update:**
1. Restore the data to the memory when the remaining space of the buffer cannot be obtained before modifying the storage buffer


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v04
**Function & Feature Update:**
1. Fix the false alarm problem of virtual ignition


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v03
**Function & Feature Update:**
1. Dormancy report When the GPS is turned on, the GPS related data will not be updated, and the data before dormancy will be reported.


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v02
**Function & Feature Update:**
1. Increase ROM space to store code
2. Fix the problem of "LTES" appearing when at+qinfo? 2G network switches to 4G
3. Increase the processing when hot plugging and unplugging the SIM. After the card is pulled out, the current network registration status can be modified in time and the network can be re-registered quickly after the card is inserted again.
4. Fix the problem that the network status bit in the 0x200 data packet cannot be updated in time when the SIM is hot-swapped with power on
5. Parameter adjustment, fix the problem that the parameter area is modified after the updated version


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.1_v01
**Function & Feature Update:**
1. Add whether to register, authentication process can be configured, at+loginmode 1: close registration, authentication 0: open registration, authentication by default
2. at+ip? command management server information removal
3.0xF7 battery information changed to mask configuration
4. Add network standard report in 0x200 message status bit


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v24
**Function & Feature Update:**
1. Electronic fence problem modification
2. Tow mode problem modification


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v23
**Function & Feature Update:**
1. Fix the problem that the module is not closed due to the timeout of the QPOWD instruction
2. Fix the problem that there is no virtual ignition message in driving mode
3. Modify the inflection point log keyword to AngStart:
4. Add GPS speed log <-- Position.Speed=
5. Increase the P808 protocol network standard status bit


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v22
**Function & Feature Update:**
1. Modify the OTA process (serialize ota step 1 and step 2, if the download fails, you will not try to read ota.bin again, regardless of whether the file exists)
2. Fix the problem that when the deep sleep IO wakes up, the backup server cannot receive the wakeup message


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v21
**Function & Feature Update:**
1. Fix the problem that the GPS is not turned on when the light sleep cycle wakes up. Turn on and off the GPS keywords: OpGps, ClGps
2. Fix the problem that the deep sleep cycle wakes up without grouping the package
3. Change the cycle of GPS time synchronization to 30 minutes Keyword: GPSTime
4. Fix the problem that the ota upgrade causes the wrong version
5. Fix the problem that the two-wire mode does not enter the driving mode when it is powered on
6. Fix bugs in QIOPEN timeout and URC processing functions
7. Fix the problem that the backup server cannot receive the ACC ignition message when the deep sleep ACC wakes up


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v20
**Function & Feature Update:**
1. Fix the configurable problem of turning on GPS time in light sleep mode
2. Fix the problem that wifi scanning is turned on when the deep sleep cycle wakes up
3. When modifying relayMode = 0, AT+GPIOVALUE configuration fuel pin does not take effect
4. Add debugging information for the problem that the GPS positioning display is yes, but the number of satellites is 0
5. Fix the problem of AccOnTime statistics error


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v19
**Function & Feature Update:**
1. Added function: AT+SLEEPGPSSWITCH=1, the time to turn on GPS in light sleep mode can be configured AT+OPENGPSTM, default value: 0 unit: second
2. Remove the query after the VM qisend location packet is sent
3. Added function: Whether to enable GPS for sleep cycle reporting can be configured according to the command AT+SLEEPGPSSWITCH 0: Disabled 1: Enabled
4. Fix the problem that the OTA_OK message is reported when the OTA is not successful
5. Fix the problem that there is no OTA_START message when performing OTA while driving
6. Weak network storage blind zone and reset restart time signal threshold value changed to 8
7. OTA problem modification, OTA process will not enter dormancy
8. Fix the problem of not restarting after receiving no reply from the server for a long time
9. Modify the deep sleep cycle to wake up and only turn on the system light
10.bugfix: The voltage threshold of the platform issued parameters is 0


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v18
**Function & Feature Update:**
1. Add 5s to print the minor version number once, subV:
2. Fix the problem that the first packet of data backup server cannot receive after waking up from deep sleep
3. Fix the problem that QIOPEN:561 cannot connect to the server continuously


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v17
**Function & Feature Update:**
1. Optimize the problem of grouping packets and dual servers after the wake-up of the two-line sleep cycle
2. When the AT command and the platform issue configuration driving voltage, parking voltage, and sleep voltage for low voltage detection, it will take effect immediately without restarting


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v16
**Function & Feature Update:**
1. Add two sleep scenarios: <1>. After the two-line sleep cycle wake-up report is completed <2>. After VCC is removed
2. Optimize the restart mechanism if the server fails to receive a reply
3. Optimize the blind zone mechanism in the weak network environment
4. Add the option to turn off Bluetooth printing
5. Increase Tmr thread stack space to 2KB
6. Modify the problem that the reporting interval caused by time synchronization is very small


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v15
**Function & Feature Update:**
1. ACC interrupt reconfiguration, ACC ignition off reporting logic optimization
2. Fix the problem that the startup package does not report
3. Get a CSQ every time you wake up from sleep
4. Fix the problem that WIFI is turned on during light sleep


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v14
**Function & Feature Update:**
1. The default value of CSQ is changed to 98 after power-on, which is different from 99 after command query
2. The ACC pin GPIO 16 does not seem to support double-edge interrupts at present. The reason is unknown, so avoid it first, and then confirm with the chip manufacturer
3. The ADC value is also obtained once in each package process
4. Limit the size of the dead zone


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v13
**Function & Feature Update:**
1. Bluetooth problem modification
2. ACC OFF message problem modification


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v12
**Function & Feature Update:**
1. Modify the CSQ critical value of the weak network storage blind zone to be less than or equal to 10, or when it is 99
2. Modify the starting position of the periodic packet timer, and fix the problem of large packet interval caused by the operation blind area
3. Modify the maximum timeout period of QICLOSE to 3 seconds
4. Modify the maximum timeout period of QFREAD to 1 second


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v11
**Function & Feature Update:**
1. Increase the weak network environment data packet direct storage buffer mechanism
2. The query time of QIRD buffer is fixed, once every minute
3. Inflection point trigger optimization
4. Bugfixes in special scenarios of QIOPEN
5. The reporting interval cannot be set to 0
6. The maximum timeout time of QIOPEN is changed to 3s


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v10
**Function & Feature Update:**
1. Query QIRD buffer time interval modification


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v09
**Function & Feature Update:**
1. Increase the processing of QIOPEN return values 563 and 566 to prevent the network socket from entering an infinite loop and failing to connect to the server
2. Increase the timing to restart the system when no reply from the server is received
3. 0XF7 normalized report in 0x200 packet
4. Fix the CSQ value of 99 in the dormant state, and now use the CSQ value of the last non-sleep state
5. There will no longer be management server information when modifying AT+QINFO query
6. Fix the problem of multiple false positives at the inflection point
7. Fix the phenomenon that the number of GPS satellites is not 0 when non-GPS effective positioning
8. Repair the uncharged status 0x01 in the battery additional information 0XF7 battery charging status in the 0X200 package
9. Fix the problem of reading blind area
10. Avoid various abnormal problems in the system caused by insufficient memory, and increase the debugging LOG
11. Increase the stack size of the timer thread to prevent the crash caused by stack overflow
12. Modify the priority of the app msg task to be the highest to prevent the package process from being interrupted by other threads, resulting in incorrect intervals
13. Do not send QADC instruction when modifying the package, and directly obtain it through the global variable, because the package period is 5s, and the main function polls once every 5s, resulting in duplication
14. Modify the qisend query to query once every 400ms, and save the blind area if the query is less than 5 times; now it takes 2s, and the original 3s will cause the process to lag
15. Add a time synchronization in the group cycle package
16. Fix module restart problem causing packet loss
17. Fix the abnormal packet time interval caused by the timeout of QFLDS and QIDEACT instructions
18. Failed to modify the memory blind area caused by the QFWRITE problem
19. Modify the maximum length of SMS to 150 bytes
20. Increase the printing when the data is stored in the blind area
21. Modify the sleep heartbeat and sleep report cannot be 0; when it is 0, there is an endless loop
22. Modify the maximum waiting time of QIOPEN to 3 seconds
23. The management server is not configured by default
24 Fix the problem of abnormal restart caused by thread stack overflow
25. When the internal battery is powered, the voltage value is changed to 0
26. Battery charging, full report optimization
27. Timing restart function optimization to prevent repeated reporting
28. FOTA upgrade version name with _beta name can also be upgraded
29. SMS FOTA upgrade stepping memory problem modification, the length of the array becomes larger
30. The processing function when the QIOPEN instruction returns 553
31. Modify the AT command array out of bounds and step on the memory problem
32. GNSS related raw data debugging LOG delete


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v08
**Function & Feature Update:**
1. Increase the electronic fence function
2. Increase ROM code space
3. Optimize charging reporting logic
4. GPIO pin modification


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v07
Release Date: 
Mon Aug 15 14:34:07 2022
**Function & Feature Update:**
1. 0x8103 package stepped on the memory problem modification
2. Optimization of packet loss problem in 5s sending cycle


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v06
Release Date: 
Fri Aug 12 09:42:35 2022
**Function & Feature Update:**
1. Optimization of distance trigger reporting
2. Restart trigger report
3. Collision trigger report, at command: AT+CRASHRANGE
4. Fixed the problem of not reporting periodic packages in special scenarios
5. When the battery is charging or fully charged, it will trigger a report
6. Optimized trailer function
7. Timing restart function is added, command: AT+RESETTIME unit: h
8. AT command sets RELAYMODE as a limit, only 0 or 1, 0 oil circuit mode, 1 normal GPIO mode
9. NETMODE is configurable, AT+NETMODE
10. Modify sscanf issues such as latitude and longitude, altitude, speed, and direction angle in GPS data analysis
11. The problem of EG915 and BG95 sending short messages has been modified, and the character sets used by the two are different
12. Added JAMMING function
13. The status bit of the oil circuit in the message increases
13. Additional information 0XF7 added in the message


**Release Version:**
AOVX_VX3xx-XX_H2.0_V2.0.0_v05
Release Date: 
Thu Aug 4 15:39:33 2022
**Function & Feature Update:**
Fixed the bug that the platform sent ota errors


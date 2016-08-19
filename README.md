= Data Taking Procedure - Main Page =

 * In case of an emergency: Call your nearest expert. You often have no rights to repair something.
 * Download and print this list of numbers in case your network fails during your shift. --> a link to a single pdf.

== Before first shift: ==

 * Ask your nearest expert for a computer account in La Palma.



|| have a working and charged phone at hand ||  ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| have important phone numbers printed at hand ||  ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| Begin one hour before datataking ||  ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| open || [https://www.fact-project.org/smartfact Smartfact] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || [http://www.fact-project.org/showlog showlog.php] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || weatherinfo see [https://www.fact-project.org mainpage] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| create new thread in [https://www.fact-project.org/logbook/forumdisplay.php?fid=2 logbook] || start Shift summary ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| connect to La Palma ||  establish VPN-connection ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || ssh to newdaq ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || screen on newdaq ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || vnc to gui ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || vnc to aux ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| plan schedule || edit schedule file (e.g. schedule.js) ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || don't forget Startup and Shutdown ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || insert schedule to DB (from newdaq) ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || write planned schedule in shift summary ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| telescope status || start tpoint CCD (via page 10.0.100.230)  ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || check telescope status in [https://www.fact-project.org/cam IR cam] and tpoint CCD (aux) ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| container status || check [https://www.fact-project.org/munin/gate/gate/container_temp.html container temperature]  ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| weather conditions || write weather conditions (allsky cam and magicweather) in logbook entry ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|||| **Startup** ||
|| Start Drive || [https://www.fact-project.org/smartfact/#control-drive smartfact drive-control] or PWR_CONTROL/TOGGLE_DRIVE ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| unlock drive || [https://www.fact-project.org/smartfact/#control-drive smartfact drive-control] or DRIVE_CONTROL/UNLOCK ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|||| **Datataking** ||
|| start datataking script || ''dimctrl --start scripts/Main.js'' or [https://www.fact-project.org/smartfact/#control-main smartfact control] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| write logbook entries ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| monitor the system || document problems or strange behaviour in logbook ||  ||  ||  ||  ||  ||  ||  ||  ||
|| monitor the weather || document weather conditions in logbook ||  ||  ||  ||  ||  ||  ||  ||  ||
|| monitor the currents || adapt schedule, if necessary ||  ||  ||  ||  ||  ||  ||  ||  ||
|| monitor the QLA Website || report interesting results in logbook[[BR]] call Dani or Adrian in case excessrate > limit ||  ||  ||  ||  ||  ||  ||  ||  ||
|||| **In case of problems** ||
|| for single runs: add comments to the Run-comment DB || [https://www.fact-project.org/run_db/db/run_comment.php Run-comment DB] ||  ||  ||  ||  ||  ||  ||  ||  ||
|| first get data taking running again || ||  ||  ||  ||  ||  ||  ||  ||  ||
|| then document problem in detail || ||  ||  ||  ||  ||  ||  ||  ||  ||
|||| **Shutdown** ||
|| stop datataking script || ''dimctrl --stop'' or from [https://www.fact-project.org/smartfact smartfact] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|||| **Check status of telescope** ||
|| no script running? || ''dimctrl --stop'' or from [https://www.fact-project.org/smartfact smartfact] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| biasvoltage off? || BIAS_CONTROL/SET_ZERO_VOLTAGE ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| trigger off? (ftmctrl should be in state Idle or Valid) || FTM_CONTROL/STOP_TRIGGER ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| telescope status? || check telescope status in IR cam and tpoint CCD[[BR]] (If it is too dark outside switch on the IR-Lights)||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| telescope parked? || [https://www.fact-project.org/smartfact/#control-drive smartfact drive-control] or DRIVE_CONTROL/PARK ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| lid closed? || LID_CONTROL/CLOSE ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| biasctrl disconnected? || BIAS_CONTROL/DISCONNECT ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| logbook entries finished? ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
||  || stop tpoint CCD (via page 10.0.100.230) ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| **stop Drive** ||  [https://www.fact-project.org/smartfact/#control-drive smartfact drive-control] or PWR_CONTROL/TOGGLE_DRIVE ||  ||  ||  ||  ||  ||  ||  ||  ||  ||
|| fill shutdown checklist || [https://www.fact-project.org/Checklist shutdown checklist] ||  ||  ||  ||  ||  ||  ||  ||  ||  ||


**Remarks** 

* Read the complete manual, not only the check list!
* Prepare for your shift well in advance!
* Start well in advance so that you still have time to contact the experts in case of problems or questions. 

----

== Startup ==

**Please use your private account for data taking. Login as *fact* user only when you really have to access the screen session with the programs, which normally not the case. You can use the *follow.sh programname* to follow the log-file of any program or the web-interface. You can do all necessary operations like starting a script from your user account or smartfact. You can check the container temperature in Munin. Using the
*fact* account you only risk to interfere unintentionally with data taking by e.g. pressing Ctrl-C in the wrong screen-tab.**

0. open Smartfact - you can monitor and operate the system from there 
0. open the gtc-skycamera image and the weather station of Magic (see https://fact-project.org/). More very helpful information like the ING infrared skycam or the TNG dust measurement can be also found there in the section "Weather Info"
0. open the page http://www.fact-project.org/showlog/index.php (for checking the logfiles)
  - use your own account for this and not the fact user!
  - different logs can be checked by adding the name of the program, e.g. http://www.fact-project.org/showlog/?log=dimserver or https://www.fact-project.org/showlog/?log=magiclidar 
  - alternatively change directory to ~fact/operation and do *follow.sh programname*, e.g. *follow.sh dimserver* (to follow the output of the dimserver which is processing the scripts)

additional information:
- [[https://www.fact-project.org/logbook/showthread.php?tid=828|Introduction for a VPN session]] gives a helpful introduction for a VPN session to La Palma - you need this to access internatl websites and don't need tunnels to access the vnc-sessions
- The screen session on newdaq has most programs running
- See ScreenSessionHelpfulCommands for a list of helpful commands for screen sessions
- On aux there is a vnc-session for the drivesystem (with the tpoint camera) and on gui one for the old gui. More details on [wiki:TroubleShootingSoftware] To connect to a vnc-session you may use a vncviewer of your choice, e.g. ''vinagre aux:1'' To find out which desktop number to connect to, you can do ''ps aux | grep vnc'' on aux and look for the :X in the command where X is the number of the desktop.

4. start the Shiftsummary in the logbook:

=== Logbook - Shift summary ===

The shift summary (first entry) has to contain the following information:

- contact details
- planned schedule
- achieved schedule
- problems
- ORM alerts

See [[TemplateShiftSummary|Template for Shift Summary]]

5. plan the schedule:

=== Schedule ===

The observation schedule is filled on the [[http://www.fact-project.org/schedule/|shedule web site]]. A automatic observation scheduler fills in a first educated guess for each night. 
The reasoning of the automated observation scheduler can be found [[http://www.fact-project.org/dch/scheduling.php|here]], by pressing the '+' sign next to 'Suggested Schedule'.

- We take a look at the suggested schedule and report and modify the schedule in case the automatic observation scheduler obviously fails.

In addition to the educated guess of the automatic observation scheduler, we need to fill in a ratescan observation.

- We add a ratescan observation to the [[http://www.fact-project.org/schedule/|schedule]] which should take place around mid night.
- A ratescan should be scheduled every third night only.
- The ratescan should be done, while pointing to the next source on schedule. This is different than the last 5 years. We want to be able to compare normal ratescans and ratescans on data.

 

To gain most out of the multi wavelength observations, we want to adopt our observation schedule to overlap with the [[http://swift.gsfc.nasa.gov/|SWIFT]] [[http://www.fact-project.org/scheduling/2016/05/24/swift.schedule.formated|observation schedule]]

When SWIFT is observing one of our scheduled sources during FACT's observation window, then we modify the FACT observation schedule to maximize the temporal overlap of SWIFT and FACT. A short summary of SWIFT and FACT overlap can be found [[http://www.fact-project.org/dch/scheduling.php|here]] when clicking on the '+' sign next to 'from Swift Schedule'.

- We take a look in the [[http://www.fact-project.org/scheduling/2016/05/24/swift.schedule.formated|SWIFT schedule]] and adjust the [[http://www.fact-project.org/dch/scheduling.php|FACT schedule]] to maximize observation overlap.

Now the schedule is ready. For more details on scheduling look [[https://trac.fact-project.org/wiki/Protected/Observations|here]]. 

6. Check status of the Telescope in the TPoint Camera (in cosy on aux; switchable on 10.0.1002.30 La Palma Network (-> you need vpn connection)) or Lid Camera http://fact-project.org/cam/lidcam.php and the [[https://fact-project.org/cam/index.php|IR Camera]]
0. Check status in the container (via the program temperature or munin)
 - if the temperature in the container exceed 40°C don't start the drive
 - wait until the temperature decreases below 40°C, maybe you can ask someone on La Palma to open the container door
0. Check weather conditions, by checking the informations from the magicweatherstation, from the tng dust measurement and from the GTC allsky camera
   - insert the informations (including the image from the allsky cam) in the logbook entry
0. switch on drive and unlock it: either from smartfact or from dimctrl:
   - start dimctrl client in any terminal: ''/home/fact/operation/**dimctrl**''
   - Power Drive:
     - PWR_CONTROL/TOGGLE_DRIVE
   - unlock Drive:
     - DRIVE_CONTROL/UNLOCK
   - stop dimctrl: .q
0. All other task of the startup are performed by the Main.js script (see first point of Datataking)
 - The list of the ManuallyStartup is currently **not** needed
 - Note that once the script is started, there is no need to stop it to change the schedule. You can change the schedule at any time. You can even start Main.js before you update the schedule (but make sure the last schedule in the database is at least 10 hours ago.

----

== Datataking ==

- start Datataking script Main.js from smartfact or from a bash with following command in ''/home/fact/operation'':
 - dimctrl --start scripts/Main.js
- if you have to start a dim-script, java-script or command for yourself, can call it with following command from a bash:
 - dimctrl --batch !ScriptsForDimCtrl/<scriptname>.dim (for a dim script)
 - dimctrl --start scripts/<scriptname>.js (for a javascript script)
 - dimctrl --quit --command ".js scripts/updateSchedule.js" (javascript via command)
 - dimctrl --quit --command "DRIVE_CONTROL/UNLOCK" (single command)
- Monitor the system be aware of the DatatakingLimits
- If you have to track manually (the script sends the tracking commands, so the manually tracking is **not** needed normally), have a look at the CurrentPointingPositions
- To control the hardware remotely, please have a look at RemoteControlHardware
- For details of the different procedures of the datataking, see the DatatakingProcedures
 - be aware that all steps mentioned there are currently proceeded by the scripts and it is **not** needed to perform them manually.
- You can find the list of the taken runs at: https://www.fact-project.org/smartfact/#observations
- Monitor the [[http://fact-project.org/dch/qla.php?expert=yes | QLA-website]] and give an alert in case of high excess rates
 - look in the [[http://www.fact-project.org/logbook/forumdisplay.php?fid=5 | Shift-Forum]] to get a trigger criterium for an alert
- don't forget to write the corresponding logbook entries and the comments in the run-comment DB:

=== Logbook - Datataking entries ===

General remarks:

- Datataking has first priority, so first solve an occuring problem, then write the logbook entries
- please fill the logbook as soon as possible (so first Problem solving, then immediatly logbook entries), so that the timestamp of the entries are correct
- make a single entry for every measurement you do (one entry for every source, for every technical measurement ...)
- insert following informations
 - weather: skybrightness, clouds, calima, ... i.e. any information that cannot be retrieved from the auxiliary files
 - please report also mistakes or missing information in the manuals so that they can be fixed/added
- for a [[SpecialRatescans|ratescan]] please insert the following informations:
 - position (Ra, Dec)
 - Zd angle
 - screenshot of the [[SpecialRatescans|ratescan]] (in smartfact or in the GUI)
 - if a ratescan looks strange, please schedule another one
 - the quality of a ratescan can be checked at https://www.fact-project.org/dch/ratescans.php
- if a problem occurs, please write down following:
 - what happens, please do not only post the error message, but also some lines above
 - what you did, to solve the problem
 - how log you need to solve the problem

TemplateNormalDatatakingSet

TemplateQuotingLogFiles

=== Run comment DB - Entries ===

- **problems / information for single runs have to be inserted in the [[https://www.fact-project.org/run_db/db/run_comment.php|run-comment DB]]**
 - these are for example:
 - fad losses
 - tracking stops
 - car flash


----

== Trouble Shooting ==

- **never** stop a not hanging program with ''ctrl+c''
 - when a restart of the program is really necessary use .q instead
 - if the program is started without console, you can try to restart with *dimctrl --restart SERVER_NAME* (SERVER_NAME might, e.g., by FAD_CONTROL) or to exit do *dimctrl --cmd "SERVER_NAME/EXIT 0"*
 - restarting a program is in most cases not a solution and only increase the risk to trigger more problems. So avoid restarting programs as long as possible 
- TroubleShooting
- List with known Hardware problems: https://trac.fact-project.org/wiki/KnownProblems)

Most common problems:

- [[troubleshooting#tsfadloss FAD losses]]
- [[TroubleShootingDrivectrl#DriveControlError | Drive Error]]

----

== Shutdown ==

[[ManuallyShutdown | manual shutdown procedure, in case it cannot be done with Main.js  ]]

0. After the shutdown task in the schedule was proceeded you have to do the the following task to finish the shutdown:
0. stop datataking script with following command from a bash:
 - dimctrl --stop
0. make sure that
 - no script is running
 - the bias is off
 - the trigger is off
 - the lid is closed
    - check TPoint Camera
    - if it is too dark outside you can switch on the IR-Lights via the [[https://fact-project.org/cam/index.php|FACT IR-Webcam page]]
    - stop TPoint Camera after check (via the page 10.0.100.230 from the internal network)
 - the telescope is parked
   - check [[https://fact-project.org/cam/index.php|IR Camera]]
 - biasctrl disconnected
 - all logbook entries are finished
0. stop the drive by:
 - in dimctrl: PWR_CONTROL/TOGGLE_DRIVE
0. Please fill out the shutdown Checklist: http://fact-project.org/Checklist/
 - make sure you have already chosen and informed someone to check you shutdown everything ok: use them in the "Nominated Checker's Email" field.

If you have to shutdown the hardware on the island, please look at HardwareManuallyShutdown
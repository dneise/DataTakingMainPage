= Data Taking Procedure - Main Page =

 * In case of an emergency: Call your nearest expert. You often have no rights to repair something.
 * Download and print this list of numbers in case your network fails during your shift. --> a link to a single pdf.
 * You are not responsible for the observation schedule, the schedule is filled automatically.

== Before first shift: ==

 * Ask your nearest expert for a computer account in La Palma.

== On your shift: ==

 * Begin well in advance (1h), so in case of problems, you can call an expert and fix stuff.
 * open
  * https://www.fact-project.org/smartfact Smartfact
  * http://www.fact-project.org/showlog
  * http://www.magic.iac.es/site/weather/index.html
 * Check some things before you start:
  * Is the weather ok to start? check:
   * http://fact-project.org/cam/index.php
   * http://fact-project.org/cam/lidcam.php
  * Is container too hot? Above 40°C the drive might make problems, do not start the drive then.
   * check it on smartfact; here: http://fact-project.org/smartfact/index.html?sound#temperature

 
 * Create a new logbook thread 
 * Note stuff, which I do not understand ... since everything is logged.
 * After shutdown in the morning: stop Main.js and do the https://www.fact-project.org/Checklist.

== In case of problems ==

 * If the Main.js script throws an exception and stops ... note down the trace back and restart Main.js
 * Do not do this crazily often, if restarting does not help:
   * note that you shutdown early due to problems.
   * park the telescope and shutdown the bias voltage.
   * close the lid
   * maybe write a mail trough fact-online, so experts are really aware there is work for them.
   * go to sleep
 * If you cannot close the lid: leave it open.
 * If you cannot shutdown the bias voltage: call an expert.
 * If you cannot park: call an expert.


== Startup via SmartFact ==

 1. Toggle Drive
 2. Unlock Drive
 3. Start Main.js 


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
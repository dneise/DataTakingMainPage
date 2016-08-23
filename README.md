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


== Stop via SmartFact ==

After successful automatic shutdown:
  * parked
  * lid closed
  * bias voltage off
  * drive off

you simply shut off Main.js

If there was an exception during automatic shutdown restarting Main.js sometimes does not help very much.
Many experts are awake at this moment, so simply call them.
If you want to deal with the situation yourself, you can try:

  * Park manually (drive must be powered and unlocked for this)
  * Close lid again (maybe open and close)
  * if parked, but the drive is not off, just toggle drive again.


Then fill out the shutdown Checklist: http://fact-project.org/Checklist/


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


# FACT - Data Taking Manual

 First Time? Ask your nearest expert for a computer account in La Palma.
 
 Print the [list of important phone numbers](https://trac.fact-project.org/wiki/Protected/ContactInfo).
 
## Your Shift:

 * Begin about 1h before startup in [tonights schedule](https://www.fact-project.org/schedule/), so in case of problems, you can call an expert and fix stuff.
 * open:
  * [smartfact](https://www.fact-project.org/smartfact)
  * [the logfiles](http://www.fact-project.org/showlog)
  * [the weather](http://www.magic.iac.es/site/weather/index.html)
 * Check some things before you start:
  * Is [the weather](http://www.magic.iac.es/site/weather/index.html) ok to start?
  * Does [the telescope](http://fact-project.org/cam/index.php) look okay?
  * Does [the lid](http://fact-project.org/cam/lidcam.php) look okay?
  * Is [the container temperature](http://fact-project.org/smartfact/index.html?sound#temperature) lower than 40°C?
 * Create a [new logbook thread](https://www.fact-project.org/logbook/newthread.php?fid=2)

 * When it is dark enough and all is clear: Start up the telescope
  1. Toggle Drive   [How?](https://github.com/404)
  2. Unlock Drive   [How?](https://github.com/404)
  3. Start Main.js   [How?](https://github.com/404) 
 
 * Observe
  * Take notes in the logbook [How?](https://github.com/404) 
 
 * Shutdown

  1. After successful automatic shutdown, simply shut off Main.js and fill out [the Checklist](http://fact-project.org/Checklist/)

  2. If there was an exception during automatic shutdown, restarting Main.js sometimes does not help very much. Many experts are awake at this moment, so simply call them. If you want to deal with the situation yourself, you can try:

   * Park manually (drive must be powered and unlocked for this)
   * Close lid again (maybe open and close)
   * if parked, but the drive is not off, just toggle drive again.
   * then fill [the Checklist](http://fact-project.org/Checklist/)

 
## In case of problems - No Panic

 First an foremost. You are a shifter, not an expert, so in case the automatic procedures fail
 and there is a problem, you might not be able to solve it.

 If the Main.js script throws an exception and stops ... note down the trace back and restart Main.js. Do not do this crazily often, if restarting does not help: [park the telescope](ManualIntervention.md) and go to bed.

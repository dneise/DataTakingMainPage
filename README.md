# FACT - Data Taking Manual

## First Time? 
 * Ask your nearest expert for a computer account in La Palma.
 * Print the [list of important phone numbers](https://trac.fact-project.org/wiki/Protected/ContactInfo).
 * Install [Anaconda](https://www.continuum.io/downloads) for the next two (at least we **strongly** recommend that)
 * install [the shifthelper](https://github.com/fact-project/shifthelper/)
 * install [la palma overview](https://github.com/fact-project/la_palma_overview)
 * (if you like:) install [Telegram](https://telegram.org/) on your phone or the [Desktop apps](https://telegram.org/apps)

## Current Problems:

### Lid Actuators Hall Sensors broken - State Inconsistent

The Hall sensors of our Lid Actuators are broken and deliver fixed random numbers. This is no problem since the motors also have end switches build into them and a current limit checked by the controlling arduino. So for opening and closing we simply drive them until either the endswitch is hit (current falls to zero) or the lid is pressed nicely shut (current rises until limit is reached). 
However the Lid Arduino software does not know about this and sometimes complains about it. This results in a `Lid control` state called `Inconsistent` on the [status page](http://fact-project.org/smartfact/index.html?#status).
The automatic control software `Main.js` knows that `Inconsistent` equals `Closed` and does not care. But sometimes people care. So please simply ignore this.

## Your Shift:

 * Begin about 1h before startup in [tonights schedule](https://www.fact-project.org/schedule/), so in case of problems, you can call an expert and fix stuff.
  * start `la_palma_overview_video` on your machine
  * open [smartfact](https://www.fact-project.org/smartfact)
  * open [the logfiles](http://www.fact-project.org/showlog)
  * open [the weather](http://www.magic.iac.es/site/weather/index.html)
 * Check some things before you start:
  * Is [the weather](http://www.magic.iac.es/site/weather/index.html) ok to start?
  * Does [the telescope](http://fact-project.org/cam/index.php) look okay?
  * Does [the lid](http://fact-project.org/cam/lidcam.php) look okay?
  * Is [the container temperature](http://fact-project.org/smartfact/index.html?sound#temperature) lower than 40°C?
 * Create a [new logbook thread](https://www.fact-project.org/logbook/newthread.php?fid=2)

 * When it is dark enough and all is clear: Start up the telescope
  1. Toggle Drive   [How?](http://fact-project.org/smartfact/index.html?#control-drive)
  2. Unlock Drive   [How?](http://fact-project.org/smartfact/index.html?#control-drive)
  3. Start Main.js   [How?](http://fact-project.org/smartfact/index.html?#control-main)
  4. Start the `shifthelper <your phone number>` [How?](https://github.com/fact-project/shifthelper/#use) [Why?](https://github.com/fact-project/shifthelper#fact-shift-helper)[Long answer.](https://github.com/fact-project/shifthelper/blob/master/rationale.md)
 
 * Observe
  * Take notes in the logbook [How?](https://github.com/404) 
 
 * Shutdown

  1. After successful automatic shutdown, simply shut off Main.js and fill out [the Checklist](http://fact-project.org/Checklist/)

  2. If there was an exception during automatic shutdown, restarting Main.js sometimes does not help very much. Many experts are awake at this moment, so simply call them. If you want to deal with the situation yourself, you can try do do some [manual interventions](ManualIntervention.md)

  3. Stop the `shifthelper` with `Ctrl-C`
  4. [Stop Main.js](ManualIntervention.md#stop-any-running-script)
  5. Stop the `la_palma_overvie` with `Ctrl-C`

 
## In case of problems - No Panic

 First an foremost. You are a shifter, not an expert, so in case the automatic procedures fail
 and there is a problem, you might not be able to solve it.

 If the Main.js script throws an exception and stops ... note down the trace back and [restart Main.js](ManualIntervention.md#start-mainjs). Do not do this crazily often, if restarting does not help: [park the telescope](ManualIntervention.md) and go to bed.

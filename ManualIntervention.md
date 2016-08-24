# Parking the telescope 

So ... the automagic parking did not work, and you are trying to do it more or less manually?
Maybe first, switch on the IR Leds of the IR cam and make sure the telescope is really not parked.
Sometimes it is actually parked but not quite (Position not reached in so and so many steps). 

It's pretty easy:

 * [Make sure no script is running](ManualIntervention.md#stop-any-running-script)
 * Start the dedicated `Stop Telescope` script [here](http://fact-project.org/smartfact/index.html?#dodrivepark)

If it doesn't work, maybe the automagic shutdown already went as far as:
 * shutting down drive power or
 * locking the drive.
 
In that case you need to manually power the drive and unlock it to try parking again.

## If this does not work:
 
If the telescope is not parked when the sun comes up and the sun shines nicely into the mirror, we might burn the camera or worse create a fire
on the telescope site. So this is a rather dangerous situation. However fear not, there are many ways to solve this. 
For you as a shifter, the first thing to do is calling an expert. 
Since in the absolute worst case it might be necessary to manually crank the telescope into parking position, which takes time,
please do not hesitate to call an expert during the night. The expert will take over from here on.


# Closing the Lid

 If you need to close the lid again, maybe first make sure it is really not closed.
 Switch on the IR Leds of the IR cam and have a look at the Lid cam.
 
 * [Make sure no script is running](ManualIntervention.md#stop-any-running-script)
 * You can control the Lid manually [here](http://fact-project.org/smartfact/index.html?#control-lid)

 ## If this does not work:
 
 Simply leave the Lid open and note it down in the logbook. Maybe send a mail through fact-online, so experts are really aware there is work for them.
 

# Shutdown the Bias voltage

In contrast to the other to manual interaction above, here `Main.js` must be running for this to work.
So make somehow sure Main.js is currently running. Then you can [switch off the voltage here](http://fact-project.org/smartfact/index.html?#irqOff)

## If this does not work:
 
If the telescope is parked and the Lid is closed, there is usually no problem in leaving the bias voltage on for some time.
Go to bed and make sure to call an expert in the morning. There are many ways to cutting the power to this system, so an expert will find a way to kill the power here.
No problem.

# Start Main.js

You can only start a script, when currently no script is running, see [Stop any running script](ManualIntervention.md#stop-any-running-script).
To start Main.js go [here](http://fact-project.org/smartfact/index.html?#control-main) and click on the [tiny little play button `>`](smartfact_lower_right_corner_play.png).


# Stop any running script

You can stop any currently running script by pressing the little white X ![the little white X](smartfact_lower_right_corner.png) on [any smart fact page](http://fact-project.org/smartfact/index.html).
You can check if a script is running by asserting that `Dim Control` appears `Idle` on the [status page](http://fact-project.org/smartfact/index.html?#status)

# R2M - a Raceroom to MoTeC telemetry exporter

**R2M** is a telemetry recorder/exporter for the Raceroom simulator. It logs and saves telemetry in a format readable by **MOTEC i2**.

**R2M** only records telemetry channels related to setups and driver development.  

### Features
 - Very low CPU and memory usage
 - Low-jitter sampling
 - High-frequency recording of suspension, wheel loads and ride height channels (200 Hz)
 - Follows the channel naming convention used by **MOTEC i2**'s built-in _Circuit Racing_ workspace, so the exported files are usable without having to configure channels

### Installation
**R2M** isn't wrapped in an installer, so simply unzip the two included files (R2M.exe and R2M.exe.config) to a suitable folder.

### Usage
![User interface](https://github.com/KrisP69/R2M/blob/main/R2M_UI.PNG)

Click the `Start` button to begin a logging session. If Raceroom isn't running when the `Start` button is clicked, **R2M** will wait and begin logging when the player's car enters the track. 

The recording of telemetry is stopped and written to the chosen destination folder when either:

- The `Stop` button is clicked
- The track session is exited
- **R2M** is exited
- The pit lane is entered (either by driving into it, or by clicking "Return to garage" or "Restart session" and then clicking "Drive" in-game) 
- The number of laps requested in the `Limit number of logged laps to` option has been logged

If the `Resume logging after auto-saving telemetry` checkbox is ticked, a new telemetry recording will begin automatically (unless recording was stopped due to the `Limit number of logged laps to` option.)

If `Discard logs with no recorded lap-times` is ticked, **R2M** won't save logs where the finish line hasn't been crossed at least once. Uncheck this box if you want to log a hillclimb session. 

When Raceroom is paused, logging is temporarily halted until the game is un-paused.   
 
  
###### Disclaimer
*The author of this software is not affiliated with Sector3 Studios, KW Studios or Motec. All rights and trademarks belong to their respective owners.*

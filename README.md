# R2M - a RaceRoom to MoTeC telemetry exporter

**R2M** is a telemetry recorder/exporter for the RaceRoom simulator. It logs and saves telemetry in a format readable by **MOTEC i2**.

**R2M** only records telemetry channels related to setups and driver development.  

### Features
 - Very low CPU and memory usage
 - Low-jitter sampling
 - High-frequency recording of suspension, wheel loads and ride height channels (200 Hz)
 - Follows the channel naming convention used by **MOTEC i2**'s built-in _Circuit_ workspace template, so the exported files are usable without having to configure channels

### Prerequisites (for older Windows systems)
[.NET 4.8 Framework](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net48-web-installer)
[Microsoft Visual C++ 2022 x64 Redistributable Runtime Files](https://aka.ms/vs/17/release/vc_redist.x64.exe) 

### Installation
**R2M** isn't wrapped in an installer, so simply unzip the two included files (R2M.exe and R2M.exe.config) to a suitable folder.

### Usage
![User interface](https://github.com/KrisP69/R2M/blob/main/R2M_UI.PNG)

Click the `Start` button to begin a logging session. If RaceRoom isn't running when the `Start` button is clicked, **R2M** will wait and begin logging when the player's car enters the track. 

The recording of telemetry is stopped and written to the chosen destination folder when either:

- The `Stop` button is clicked
- The track session is exited or changed (i.e. from practice to qualify or qualify to race)
- The track session is restarted (unless session is a leaderboard challenge)
- **R2M** is exited
- The pit lane is entered (either by driving into it, or by clicking "Return to garage." An exception is hillclimb tracks because they don't have pit lanes)  
- The number of laps requested in the `Limit number of logged laps to` option have been logged

If the `Resume logging after auto-saving telemetry` checkbox is ticked, a new telemetry recording will begin automatically (unless recording was stopped due to the `Limit number of logged laps to` option.)

If `Discard logs with no recorded lap-times` is ticked, **R2M** won't save logs where the finish line hasn't been crossed at least once.
When RaceRoom is paused, logging is temporarily halted until the game is resumed.   
 
### Disclaimer
*The author of this software is not affiliated with Sector3 Studios, KW Studios or Motec. All rights and trademarks belong to their respective owners.*

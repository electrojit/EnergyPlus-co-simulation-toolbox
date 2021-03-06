# Release notes

## [todo]
 * Add support for EnergyManagementSystem:OutputVariable
 * EPW source block for Simulink.
 * Bus objects may be stored in a DataDictionary to avoid its residency in 
   the base workspace.
 * epJSON

## [unreleased] 

### Added    

### Changed
 * renamed installMlep to setupMlep. Solved a critical bug therein (v1.2.1.1).
 * 
  
## [v1.2.1] 

### Added   
 * Better documentation

### Changed
 
## [v1.2]
Bus objects generated in 

### Added 
 * Load and Save routines.  
 
### Changed
 * Bus objects are now loading in the Init function callback. It should solve 
   the '_Missing Bus objects_' issues.
 * Optimized IDF file parsing speed.
 * Initialization no longer triggered from the Simulink mask.
 * Robustified _Vector to Bus_ block callback.

## [v1.1]
Structure of the main Simulink library was changed to support signal names longer then 63 characters.

### Added
 * Bus objects now support signal names longer than 63 characters.
 * Simulation and initialization are now considerably faster. 
 * **Vector to Bus block**. Make a bus out of a apprapriately sized vector.
 * Browse buttons in the Simulink block mask.
 
### Changed
 * mlep system object does not work internally with busses anymore. It imposed the 63char. limit and was slow anyway. 
 * Renamed the main simulink block from _EnergyPlus SO_ to **EnergyPlus Simulation**.
 * The working directory is by default the directory of the selected IDF file.
 * IDF and EPW files are no longer required to be on the Matlab searchpath.
 
 ## [v1.0]
This release builds upon a _mlep_ code by Truong Nghiem and Willy Bernal.

 ### Added
 * Parsing of the IDF file to determine co-simulation inputs/outputs.
 * Automatic socket communication configuration (on localhost).
 * Background start of the EnergyPlus process with output to the Matlab command line.
 * System Object implementation usable in Matlab & Simulink.
 * Bus input/output integration for easy Simulink model setup.
 * A 'mlep Bus Creator' block to facilitate Simulink co-simulation input setup.
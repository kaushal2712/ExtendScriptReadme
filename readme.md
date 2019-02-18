# ExtendScript Debugger for Visual Studio Code

![Demo GIF](images/demo.gif)

**Supported features**
* Target and Engine Information Bar - ExtendScript Developers can launch the supported Adobe's point product and select ExtendScript engine
* Call Stack
* Breakpoints
	* Hit counts
	* Expressions
	* debugger statement
* Variable Inspection
	* Local Scope and Global Scope
	* Change a variable
* Debugging commands
	* Continue
	* stepin
	* stepover
	* stepout
	* stop
	* restart
* Debug Console
	* Expression evaluation
* Expression Evaluation on Hover
* Export ExtendScript to JSXBIN
* Target started debug session

**Unsupported scenarios**
* Profiling Support
* OMV
* Functions/Auto-Completion
* Scripts Panel

## Getting Started
1. [Install the extension](https://marketplace.visualstudio.com/items?itemName=adobe.extendscript-debug)
2. Restart VS Code and open the folder containing the project you want to work on.

## Troubleshooting

### I am getting Error ##15 Can't initialize target. What's wrong?

* Make sure the ESTK stand-alone application is closed
* Close the target application (example; Photoshop)
* Close Visual Studio Code
* Make sure there are no VS Code Helpers processes in the Activity Monitor (Mac) or Task Manager (Windows)
* Restart Visual Studio Code
* Does it work then?
* If not, does a reboot help?

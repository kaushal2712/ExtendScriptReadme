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
The following steps are good standard troubleshooting, as well as troubleshooting "**Error ##15 Can't initialize target.**"

* Make sure the ESTK stand-alone application is closed
* Close the target application (example; Photoshop)
* Close Visual Studio Code
* Make sure there are no VS Code Helpers processes in the Activity Monitor (Mac) or Task Manager (Windows)
* Restart Visual Studio Code
* Does it work then?
* If not, does a reboot help?

If you continue to run into problems, please report them in the [Forums](https://forums.adobeprerelease.com/exmancmd/categories/estkvsc)

## FAQ
**Q. Where is the actual error displayed?**

A. When you hover over the words on the line that errors, there will be a popup showing the error. The error should be there in Output Console too.

**Q. I am getting Error ##15 Can't initialize target.**

A. Please try following the steps in the Troubleshooting section above. If you continue to run into this error, please tell us about it in the [Forums](https://forums.adobeprerelease.com/exmancmd/categories/estkvsc)

**Q. Can I set the Target Application in launch.json?**

A. You can set the target application in `launch.json`. 

For this you will need target specifier. To get the target specifier, put `"trace" = true` in your `launch.json`. When you start a session in your desired application (by choosing from "Select the target application"), the first line in Debug Console/Output Console will be `Starting <yourScript> in target: <targetSpecifier> and engine: <engineName>`. You can then get these two values and put in your `launch.json` configuration: 

 ```"targetSpecifier": "photoshop-130.064", "engineName": "main" ```

 **Q. How can I avoid the `ask for name` prompt?**

A. You can avoid the 'ask for name' prompt by putting the script name into the `launch.json` file. For example, my script is named `test.jsx`:

```json
{
  "version": "0.2.0",
  "configurations": [    
    {
      "type": "extendscript-debug",
      "request": "launch",
      "name": "Testing this plugin",
      "program": "${workspaceFolder}/test.jsx"
    }
  ]
}
```





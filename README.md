# A Roblox Train Driving System - A Simple Driving System for anyone

This repository is based around a Roblox Train Driving system for anyone, no matter scripting knowledge, to use and play with.
If you'd like to get straight on with it, a .rbxm is provided in the releases, but its best you read the below.

If you are a programmer wishing to help contribute to this repository, please read down at the bottom of this.

# YouTube Video

To be updated

# Installation
To get a stable release, head to [this page](https://github.com/jake-baxter/rblx-train-driving-system/releases) this page and download a version with a stable tag.

Other versions ending with -alpha or -beta are unstable and better for simple users not to play with.

Instructions for downloading/updating will be provided with this release.

Unextract the zip file and open the readme.txt file, which will provide installation instructions.

Then import all the required .rbxms in the "required" folder, and then optional ones in the "modules" folder.

If you need a tutorial on how to do this, go up to the youtube header above.

# Setting up the train
Create a new script within the train.

You then call ```require()``` to the location of the script. Then respectively call the new function on it, see the new function area below for it.

Example:
```
local TrainModule = require(game:GetService("ServerStorage"):WaitForChild("TrainModule"))
local newTrain = TrainModule.new(
    ...
)
```

You can then used the returned table by .new()  to call other functions or register RBXScriptConnections

# Functions

## Direct Require
### ```.new(trainModel, inputTrainData)``` - Makes a new train using API
`trainModel`  Object Value of Train Model
`inputTrainData`  Table of Train Input Data (see section below)
returns `classSelf` - Dictionary of train Functions and values


## Train Functions
### ```:GetDriver()``` - Gets the current driver
returns `player` - Player object of driver

### ```:EnableModule(moduleReference)``` - Enables a Module
`moduleReference`  Object Value of appropiate module script
returns `bool` - True/False if enabled or not

### ```:DisableModule(moduleName)``` - Disables a Module
`moduleName`  String Value of model name
returns `bool` - True/False if enabled or not

### ```:SendMessage(moduleName, Table)``` - Sends a message server side.
`moduleName`  String Value of module name to send a message to or on behalf.
`Table`  Table of what you want to send
returns `bool` - Always true if no errors

### ```:SendPlayerMessage(moduleName, Table)``` - Sends a message to the driver player.
`moduleName`  String Value of module name to send a message to or on behalf.
`Table`  Table of what you want to send
returns `bool` - True if sent, false if not.
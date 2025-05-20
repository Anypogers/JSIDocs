---
sidebar_position: 2
---

# Download

JSI run completelly locally (unless you set it up to host on a dedicated server), and so, you need to download it and set it up properly.

This page will help you set it up.

## Downloading dependencies

Your going to need a couple of other tools in order to use JSI.
Note that depending on the intents you decide to use/make, you are going to need more dependencies, in wich case, you should check the intents directly for their dependencies.

**Base required dependencies: (needed to just run JSI)**
- Latest version of NodeJS

## Downloading the project

Firstly, start by getting the necessary core files from the github repo.
You have two options:

**Option 1:**
- Download the github repo as a .zip
- Extract the .zip where you want it to be saved
- Follow the rest of the instructions

**Option 2 (requires git):**
- Clone the github repo
- Follow the rest of the instructions

It's recommended to use option 2 for an easier time updating the project when need be.

## Installing the project

After downloading the project, the first thing you are going to need is to open it's folder and let it download all the Node dependencies
How to do it, open up a cmd console inside the JSI folder, and type in this command:
```bash
npm install
```

## Configuring JSI

To configure JSI, it is recommend to use the JSI Web Aplication, since it's easier to understand, and safer to use.

However, if you know what you're doing, you can just edit the file manually to change it's configuration.

To do it manually, open the file "`JustSimpleIntents/src/config.js`" in any text editor (notepad, notepad++, visual studio code, etc)
Each configuration value has comments explaining each of them. What they're used for, their default value, and some acceptable values.
Then, just change the current value to what you want, then, save and close the file.

## Running JSI

Lastly, to run JSI, open up a cmd console on the root of the JSI folder (`JustSimpleIntents/`), and run the command:

```bash
npm run start
```
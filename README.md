# check_point_windows_scripts

SmartConsole/SmartDashboard Configuration Backup Script:

Backup user profile based SmartConsole settings for R80, R80.10, and R80.20, R80.30, R80.40, and R80.50, backup registry for R77.30, R80, R80.10, R80.20, R80.30, R80.40, and R80.50.

Use this before uninstalling SmartConsole to backup settings for user.

To restore settings:
1.)	Backup SmartConsole configuration settings (run script)

  You might want to zip the directories under "%USERPROFILE%\appdata\local\Check Point\SmartConsole\" where R80, R80.10 and R80.20 keep their user specific SmartConsole settings on disk, versus just the registry keys used in pre-R80.x versions like R77.30.
  
2.)	Uninstall SmartConsole version

3.)	If asked to reboot, check “%programfiles(x86)%\CheckPoint\SmartConsole” for whether version folder exists, if yes, delete--then ignore the reboot statement.

4.)	Install SmartConsole application

5.)	[Optional] Launch SmartConsole and enter Demo mode (cloud demo)

6.)	[Optional] Once cloud demo SmartConsole is fully up and visible, exit the cloud demo SmartConsole

7.)	Restore SmartConsole configuration

  a.	Execute registry key(s) for the version installed

  b.	Restore files to local user profile location

8.)	Start SmartConsole again, all settings should be good

Supports versions:
- R77.30 - Registry
- R80    - Registry, User Profile data
- R80.10 - Registry, User Profile data
- R80.20 - Registry, User Profile data
- R80.30 - Registry, User Profile data
- R80.40 - Registry, User Profile data

Updated 2020-03-31:  Added R80.30 - R80.50 support


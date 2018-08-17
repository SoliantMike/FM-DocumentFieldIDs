FM-Document Field IDs
=================

If Field IDs get out of order across environments, it can cause unexpected results when moving files during deployments. This file is used as a tool to compare internal field IDs in two FileMaker Files and show where there are differences, as compared to their field names.

The additional "Contacts" and "Contacts 2" files are supplied to demonstrate how it works. To use in your own environments, follow the instructions below. Works on local or hosted files, so you do not need local copies.

Instructions

    1. Edit the External Data Sources to point to the files you wish to compare. 
        There should be at least two external data sources, even if they are local files.

    2. Copy the script named "-sub ReturnFIelds" from this file and Paste it into each referenced file from step 1, if it does not already exist.

    3. Update the script "Refresh Field List" and in the REPEAT section, update every script step to call the script from step 2, for each file.

    4. Run the "Refresh Field List" script. If there were errors detected, the red button will show a list of descrepancies. 

This allows you to identify and fix potential problems before pushing updates to production.
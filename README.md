# Automating a browser in Playwright to download raw data and format it into a compressed, easy-to-read visual format for use in presentations

>[!NOTE]
>The website has since changed their download functionality, so you no longer download a file, you receive it by e-mail. This breaks the pipeline in this script, because the second function expects a .csv file inside the project folder. This is easily fixed by programmatically (or manually) grabbing the file from Outlook, but I'm just noting it here because I know about the change. The download function of this script still successfully triggers the data to be e-mailed to the user, but needs minor adjustments if I want to use it with the new functionality of the website in the future.  

This is a simple script I wrote that uses Playwright to automate a Chromium browser in order to:
* Navigate to a website
* Log in
* Navigate the website's sub-menus
* Download the desired dataset with hotel statistics and save it in the project folder
* Load the data from the downloaded .csv file and format it into a compressed, easy-to-read visual format for use in presentations

Since the script requires login info, but also needs to be usable by more than one person, it simply asks for login information from the user in the PowerShell terminal window.

The output looks like this:  
![Script output](Benchmarking%20Alliance%20occupancy%20overview.png)  
The table shows the occupancy rates for hotels in a select geographic area per day, per month with specific highlights in yellow for days with lower occupancy and highlights in green for days with higher occupany. Used to figure out and showcase what times of the year that there is the most room for added tourism activity for a given year.

### Skills used:
* Playwright / Browser automation
* Python
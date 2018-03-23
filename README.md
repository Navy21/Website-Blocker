PROJECT DESCRIPTION:
This application doesn't let a person browse distractive websites like facebook, youtube during the working hours.
This project mainly focuses on file manipulation and working with dates and times.
We open host file via python using file handling methods and we can add lines of text at certain times of the day in this host file.
If the working hours are between 8.00 AM and 4.00 PM, python script runs entire day and checks every 5 minutes. 
If time falls into working hours then python adds those websites url's as lines to block these websites.
If it is past 4pm, then it will delete these lines in the host file.


PROJECT IMPLEMENTATION:
Open hosts file in python using open() method and iterate over the websites list to check if the websites are on the hosts file during working hours.
If not, then these websites along with the redirection IP addresses are written to the host file using write() method.
During non-working hours, delete the websites and redirection IP addresses from the hosts file using truncate() method.
Schedule python script to run as process on the background immediately after the computer is turned on using "Task Scheduler" and by saving the script file with ".pyw" extension.

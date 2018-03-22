# Website-Blocker: Steps to follow
This python application doesn’t let the user to browse distractive websites like Facebook, YouTube during the working hours.
Open “hosts file” in python using “open()” method and iterate over the websites list to check if those websites are on the hosts file during the working hours. If not, then those websites along with the redirection IP addresses are written to the hosts file using “write()” method.
Delete the websites and redirection IP addresses from hosts file during non-working hours using “truncate()” method.
Schedule the python script to run as a process on the background immediately after the computer is turned on using “Task Scheduler” and by saving the script file with “.pyw” extension. 

# Website-Blocker
import time
from datetime import datetime as dt

hosts_temp = r"C:\Users\Navyasree J\challenge\hosts"   # This is the copy of hosts file copied in a different location.
hosts_path = "C:\Windows\System32\drivers\etc\hosts"
redirect = "127.0.0.1"
website_list = ["www.facebook.com", "facebook.com", "dub119.mail.live.com", "www.dub119.mail.live.com", "www.amazon.com"
                "amazon.com", "www.myntra.in", "myntra.in", "www.shoedazzle.com", "shoedazzle.com"]
# any number of websites can be blocked but link has to be included without any errors.

while True:
    if dt(dt.now().year, dt.now().month, dt.now().day, 9) < dt.now() < dt(dt.now().year, dt.now().month,
                                                                          dt.now().day, 17):
        print("Do not open anything else. Time to work")
        with open(hosts_path, 'r+') as file:
            content = file.read()
            for website in website_list:
                if website in content:
                    pass
                else:
                    file.write(redirect+" " + website+"\n")
    else:
        with open(hosts_path, 'r+') as file:
            content = file.readlines()
            file.seek(0)
            for line in content:
                if not any(website in line for website in website_list):
                    file.write(line)
            file.truncate()
        print("Fun Time, Fun Hours")
    time.sleep(10)

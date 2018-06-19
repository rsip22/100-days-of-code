# 100 Days Of Code - Log

### Day 0: June 18th, 2018.

**Today's Progress**: I reviewed how to write list comprehensions in Python (thanks, Elias!) and I also reviewed how to setup the enviroment with the new pipenv, a new skill I learned not long ago when I participated in the Grupy-RN meetup. I read a bit Selenium's documentation and wrote a small script to automate the login to a Django application and save to a txt file the cookie that was generated. The first time I used Selenium, I wrote a script to the Chrome webdrive, but this time I wanted to change things a bit, so I used Firefox's (Gecko) webdriver.

**Thoughts:** I installed PyCharm and played with it for a bit, thanks to a license I was gifted during Python Nordeste. It's a bit strange to get used to using an IDE to develop. It seems this ability can be useful in the long run when I work on more complex projects, but... it takes a bit to get used to all the options and possibilities that come with it. About the code: I look forward to learning more about Selenium and using it with Python and other languages to automate boring tasks that should never be done manually. 

**Link to work:** [Auth Django](https://github.com/rsip22/101/tree/master/100daysofcode/Python/auth_django)

=========
### Day 1: June 19th, 2018.

**Today's Progress**: I wrote a small script to visit the Django Girls website and get a list of cities that have hosted workshops. As of now, this list is exported to a txt file. 

**Thoughts:**  Although there are other ways - probably *better ways* ([Requests](http://docs.python-requests.org/en/master/), [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)) to do this task, I ended up using Selenium again because it is my focus to learn more about it. I didn't want to overwhelm the Django Girls server with my requests, so I copied the source-code for the events page in a html file. At first, I put it up in a Github repository, but then I realized that this might not be needed - everything worked just fine when when I specified a local address to be accessed by Selenium. When getting the data from the website, I made a mistake writing a loop within a loop that kept the program running forever and it took me some time to debug. That's why I didn't write more of the code and created the csv or JSON export as I intended. 

**Link to work:** [Django Girls Locations](https://github.com/rsip22/101/tree/master/100daysofcode/Python/djangogirls_locations)

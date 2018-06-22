# 100 Days Of Code - Log

### Day 0: June 18th, 2018.

**Today's Progress**: I reviewed how to write list comprehensions in Python (thanks, Elias!) and I also reviewed how to setup the enviroment with the new pipenv, a new skill I learned not long ago when I participated in the Grupy-RN meetup. I read a bit Selenium's documentation and wrote a small script to automate the login to a Django application and save to a txt file the cookie that was generated. The first time I used Selenium, I wrote a script to the Chrome webdrive, but this time I wanted to change things a bit, so I used Firefox's (Gecko) webdriver.

**Thoughts:** I installed PyCharm and played with it for a bit, thanks to a license I was gifted during Python Nordeste. It's a bit strange to get used to using an IDE to develop. It seems this ability can be useful in the long run when I work on more complex projects, but... it takes a bit to get used to all the options and possibilities that come with it. About the code: I look forward to learning more about Selenium and using it with Python and other languages to automate boring tasks that should never be done manually. 

**Link to work:** [Auth Django](https://github.com/rsip22/101/tree/master/100daysofcode/Python/auth_django)


### Day 1: June 19th, 2018.

**Today's Progress**: I wrote a small script to visit the Django Girls website and get a list of cities that have hosted workshops. As of now, this list is exported to a txt file. 

**Thoughts:**  Although there are other ways - probably *better ways* ([Requests](http://docs.python-requests.org/en/master/), [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)) to do this task, I ended up using Selenium again because it is my focus to learn more about it. I didn't want to overwhelm the Django Girls server with my requests, so I copied the source-code for the events page in a html file. At first, I put it up in a Github repository, but then I realized that this might not be needed - everything worked just fine when when I specified a local address to be accessed by Selenium. When getting the data from the website, I made a mistake writing a loop within a loop that kept the program running forever and it took me some time to debug. That's why I didn't write more of the code and created the csv or JSON export as I intended. 

**Link to work:** [Django Girls Locations](https://github.com/rsip22/101/tree/master/100daysofcode/Python/djangogirls_locations)

### Day 2: June 20th, 2018.

**Today's Progress**: 
The script I wrote yesterday now exports the information from that list to a csv and to a JSON file. I played a bit and used another module ([sys](https://docs.python.org/3/library/sys.html)) from Python to specify the path for the JSON file to be saved (getting the current path). I installed and used [PyLint](https://www.pylint.org) to check my code. At first, I ran into this error:

```
E: 25, 0: Unable to import 'selenium' (import-error)
E: 26, 0: Unable to import 'selenium' (import-error)
```
Which I solved by installing pylint with pipenv. After that, I got:

```
Your code has been rated at 10.00/10 (previous run: 7.62/10, +2.38)
```

**YAY! SUCCESS!** 

**Thoughts:** To be able to write code that exports data to different formats is a very useful skill. I was bugged that for some reason I couldn't get the JSON file to be saved yesterday, but I guess I was too tired to realize I was missing the argument that specifies the file to be written in json.dump. Today, I came back with a fresh head and it wasn't hard to figure it out. I had to work on ensuring the names of the cities would be spelled correctly even when they had characters that are strange to the English language (like 'Wrocław', 'São José dos Campos' and 'Ado-Ekiti').      

**Link to work:** [Django Girls Locations](https://github.com/rsip22/101/tree/master/100daysofcode/Python/djangogirls_locations)

### Day 3: June 21th, 2018.

**Today's Progress**: I made a slight improvement to the previous script and I started learning TDD with Python and Django. 

**Thoughts:** I started reading 
["Obey the testing goat" book](http://www.obeythetestinggoat.com/pages/book.html) and following the instructions. I read the first two chapters and I can already say that I quite enjoy the way things are explained in it. Of course, it sort of helps that I do know some Django already, but I didn't feel lost with new concepts such as functional tests and unit tests so far.  

**Link to work:** [testing goat](https://github.com/rsip22/101/tree/master/100daysofcode/Python/testing_goat)
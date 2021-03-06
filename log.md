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

### Day 4: June 22th, 2018.

**Today's Progress**: I kept studying TDD with Python and Django, following 1 and a half chapter of the book. 

**Thoughts:** Today was hard to read the two chapters of the ["Obey the testing goat" book](http://www.obeythetestinggoat.com/pages/book.html) that I aim to. I did dedicate more than 2 hours to it and to coding, but I was interrupted a few times with community stuff, which meant going back to re-reading the same parts again to find the context of where I stopped. That is also why I'm commiting this after midnight (but before bed, so it definitely still counts as yesterday, right?). I'm quite enjoying learning about TDD with Django, taking each step to create the tests, fail them, and them write each bit of code to make them pass. I find it very interesting how each error gives us the next clue to the code that should be written next.  

**Link to work:** [testing goat](https://github.com/rsip22/101/tree/master/100daysofcode/Python/testing_goat)

### Day 5: June 23th, 2018.

**Today's Progress**: I kept studying TDD with Python and Django. 

**Thoughts:** Today I focused more on schematizing and writing down on my study notebook the things that I have been learning about TDD, to help grasp all the content.  

**Link to work:** [testing goat](https://github.com/rsip22/101/tree/master/100daysofcode/Python/testing_goat)

### Day 6: June 24th, 2018.

**Today's Progress**: I kept studying TDD with Python and Django. I'm on chapter 5 of the book now. 

**Thoughts:** Ugh, I got completely stuck on an error after I added the csrf_token to send the form. Instead of running the test properly, it started giving me a BrokenPipeError that I haven't found a way to get out of it. I have retraced all the steps twice and still can't find a mistake I did. I searched a lot on places like stackoverflow and the Django Documentation and still couldn't figure it out. I added allowed_hosts and it changed nothing. Maybe it's something with Django or Python 3.6? I'm wrapping things up here to see if I can figure it out when I come back with a fresh head.  

**Link to work:** [testing goat](https://github.com/rsip22/101/tree/master/100daysofcode/Python/testing_goat)

### Day 7: June 25th, 2018.

**Today's Progress**: I kept studying TDD with Python and Django. I'm still on chapter 5 because yesterday I was stuck on the BrokenPipe error, which I solved today. Today, I also started working on: testing and writing models, processing POST request and doing redirects.   

**Thoughts:** I redid all the steps from the previous chapter again, trying to figure out happened and to debug. So the BrokenPipe error actually changed not by adding {% csrf_token %}, it happened when I changed the time.sleep from 1 to 10. I went back to 1 and I finally, *finally* got the right error. I'm still on chapter 5, going to "Better Unit Testing Practice: Each Test Should Test One Thing".   

**Link to work:** [testing goat](https://github.com/rsip22/101/tree/master/100daysofcode/Python/testing_goat)
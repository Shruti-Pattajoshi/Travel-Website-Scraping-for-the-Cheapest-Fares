# Travel-Website-Scraping-for-the-Cheapest-Fares

Lets us choose the following based on our requirements : Ticket type (round trip, one way), Departure country, Arrival country (if round trip) and finally the Departure and Return dates and gives the best rate in every hour.

The project code connects Python to the web browser using that particular web browser's driver and requests access to the travel website. Beautiful Soup and Selenium work the best for the dynamic web page scraping. Beautiful Soup independently is good for the static web page scraping in DOM (document object model) while when it comes to scrape a website like a dynamic website, Selenium automates web browser interaction from python. Hence the data rendered by JavaScript links (pages connected 1- 10 for eg. ) can be made available by automating the button clicks with Selenium (after selection of dates, source, destination , type of ticket using copy XPath Selectors clicking buttons for eg. Next, Submit) and then can be extracted by Beautiful Soup. The code compiles all the available flights in a structured format which can further be useful in data analysis.

Beautiful Soup then passes on the data scraped to pandas. Pandas reads the table data into a data frame. The data frame will now have the details ( flight time, date, cost , source and destination ) which is further stored as an excel sheet for exploratory analysis. 

Then the first row ( usually the best select ) is sent by Email to the user using the smtplib library. This process is repeated 4(user dependent) in a day : sleeps for 6 hours interval. 

Further Improvements:
In the project the web driver runs the browser (visible to user) in an automated way but if we use the incognito method then the window wont be visible to the user while it is being run
Run the code on multiple websites and select the current best rate from all to the user
Using for multiple dates and finding the date the best prices are there and on which website.
Useful for Data Analysis of the dynamic flight pricing and find its relationship with what time the flight is, what weekday it is and find useful conclusions
Can send the Excel File as an attachment to the mail

Challenges : 
Choosing which platform to scrape the information from because of the reCaptchas on the websites 
Avoiding ReCaptchas Check is tough while Code Checking-Debugging

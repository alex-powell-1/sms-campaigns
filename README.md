SMS Campaigns

Author: Alex Powell

This cross platform Tkinter/Python application queries a Counterpoint POS associated SQL database for customer data and sends progrommatic 
text (through Twilio API) based on 1) single phone number entry or 2) .csv upload or 3) customer data. 

The application can send standard SMS messages or MMS with pictures.

If the application receives an API response that the number is actually a landline, it will automatically move the customer's 
phone number over to the established landline field in SQL. In this regard, the application helps clean the database.

Methods:
1) Single Phone - just enter a single phone number and it will send it directly to this number

2) .csv upload - select a csv file with the following four columns 1)CUST_NO, FST_NAM, PHONE_1, LOY_PTS_BAL
   - LOY_PTS_BAL is a balance of reward points

3) Customer Segment
Currently, texts can be sent for the following criteria:
1) Management Test Group
2) Wholesale Customers
3) Retail Customers: All
4) Yesterday's Shoppers
5) 5 Day follow-up
6) 1 week follow-up
7) Retail: Most recent 1000 customers
8) Retail: Most recent 2000 customers
9) Retail: Most recent 3000 customers
10) Retail: Most recent 4000 customers
11) Spring Annual Shoppers
12) Fall Mum Shoppers
13) Christmas Shoppers
14) No purchases in 6 months
15) No purchases in 12 months
16) By Birthday Month

The application logs the sent message history to a desired path. 

The application has a test mode that allows you to run the process without actually sending the messages through the API so you can check recipients.

Known limitations
While the application is sending texts (potentially 1000's of texts), it will print the API response to the console. I would like to implement a progress bar that shows the user the progress
so they do not exit the application prematurely. Currently, once all texts have been sent, a success message box appears and asks the user if they would like to see the log.

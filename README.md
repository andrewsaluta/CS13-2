# CS13-2
Software Design Specification
Test Line

PRESENTATION LAYER
----> Mobile application
----> Online website
----> In-Person Kiosk
APPLICATION LAYER
----> Theater API
----> User authentification
----> Server connection service
BUSINESS LAYER
----> Ticket purchasing Service
----> Location & Movie Lookup Service
----> Payment Processor (Online/In Person)
DATA STORAGE LAYER
----> User Database (tickets,etc)
----> Theater Database (Movies/Prices/Showtimes)
----> Company Database (All theater/user info metrics centralized)

EXTERNAL SERVICES LAYER
----> Payment Processing System
----> Email/text confirmation system
----> Analytics Tracker/Storage
----> Login Gateway
----> Movie statustuc monitoring service

-- DESCRIPTION -- 
OVERALL SUMMARY
This system supports movie ticket browsing and purchases through multiple different interfaces (mobile app, website, and in-person kiosk). It uses a layered architecture for the diagram including a presentation layer, Application layer, Business layer, and Data Storage layer. It also includes an external service layer for third party functions like payments, notifications, analytics, and authentification. Requests for purchases start from the user interface in presentation layer into application layer, which gets logged into the Business layer for finalizing the purchase, and finally into the Data Storage layer to keep track of the movie purchased, seat selection, and business logistics.



3 test cases

MovieBrowsing_1	Movie_Search_Module	P0	Verify that when a customer enters a Movie to search and presses enter, the correct movie is displayed.	Browser is launched	"1. Launch Ticket Processing Machine website and/or kiosk
2. Once TPM is launched, write the Movie name - ""Avengers"" in the search bar.
3. Press enter."	Search results related to 'Avengers' should be displayed	Search results with 'Avengers' keyword are displayed	Pass	TesterA
SelectionSearch_1	Selection_Search_Module	P0	User gets prompted to select seats and is prompted with a CAPTCHA to go through with the payment processing.	Browser is launched	"1. Select any Movie within the Ticket Processing Machine website or kiosk.
2. Select specific seats.
3. Enter correct CAPTCHA.
3. Make sure payment window activates."	Payment is processed and Seats should be blocked out for future customers	Payment is processed and seats are blocked out for future customers	Pass	TesterA
WebPurchase_1	Web_Purchase_Module	P0	End-to-end web purchase flow Covers browsing, seat selection, payment, and QR ticket generation in one full web transaction.	app is functional	1. Launch application in phone. - 2. Search for a movie , i.e ('Dune') 3- Select seats for a showtime for dune 4-purhcase seats 5-view qr code ticket	Search results display dune and showtimes/locations, seats are able to be selected, purchasing works correctly, qr code succesfully displays	Dune and showtimes/locations appear, seat is able to be selected and purchased, qr code is seen	Pass	TesterJ

added one sql and seat lock cache

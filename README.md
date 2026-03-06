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

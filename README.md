# Bus-Ticketing-System
The idea behind this application is to have a bus system that goes to every state

The following API’s have been used In our implementation:

Addpayment: Creates payment in database

Bookingid: Information regarding that booking

Createbooking: Creates booking in database

get-price: Price of trip

get-values: Finds if credentials are authorized

pasttrips: Grabs past trips of user

payment: Grabs payment options of user

payments: Grabs payment options for removal

removecard: Removes card from database

post-data: Adds a new profile to the database

profile: Grabs user information

profileupdate: Updates user information

refund: Refunds booking

trip: Finds upcoming trips for planned locations

upcoming: Grabs user’s upcoming trips

# Features:

Sign-in/ Registration: To use the app/website users need to login via email. It will be authorized by the data in RDS. If the user is not registered, they need to register and confirm their verification for SES to send them a confirmation email. 

Booking: Users can book their tickets by specifying their start and end location and the number of tickets required. 

Profile Update: In case the user needs to update their profile details, they can update it and RDS will update it as well. 

Payments: For any transaction, the user needs to add a credit card beforehand in the payments section of the website. They can remove/add multiple cards or update the existing one.

Travel History: Their past trips and transactional values will be stored in a separate RDS database.

Refunds: Any future trips can be cancelled, and refund will be issued to customers. 

Rewards: For any trip the users will get some rewards, depending on the range of their transaction. These rewards can be redeemed in future trips to get some discount.

# Implementation:

The hosting of static website is done on EC2 instance and Flask was used to implement the frontend of our project. The RDS database stores the user data including email and password. The user needs to login to access the app, SES will send a verification email to users. Once the user logs in, they can plan a trip, edit a future trip, add payment methods, or stream entertainment. We used Cognito for sign-up and authentication for our video streaming service. For the streaming part CloudFront is used as a CDN. The trip locations and distances are fetched from MapCrow to give an accurate cost per trip per person. Whenever a trip is planned EventBridge updates the lambda functions to store new/updated values in RDS. We used QuickSight to analyze the data in RDS to get a better understanding of users and how to improve the website. 

![SAP HANA (Single-AZ, multi-node) (1)](https://user-images.githubusercontent.com/32221934/229387888-6d12863a-8230-4b76-a6ca-81ad29c2b7a6.jpg)

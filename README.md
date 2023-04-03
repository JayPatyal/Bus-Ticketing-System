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

#Implementation:
The hosting of static website is done on EC2 instance and Flask was used to implement the frontend of our project. The RDS database stores the user data including email and password. The user needs to login to access the app, SES will send a verification email to users. Once the user logs in, they can plan a trip, edit a future trip, add payment methods, or stream entertainment. We used Cognito for sign-up and authentication for our video streaming service. For the streaming part CloudFront is used as a CDN. The trip locations and distances are fetched from MapCrow to give an accurate cost per trip per person. Whenever a trip is planned EventBridge updates the lambda functions to store new/updated values in RDS. We used QuickSight to analyze the data in RDS to get a better understanding of users and how to improve the website. 
![image](https://user-images.githubusercontent.com/32221934/229387754-9cc3fb6e-3f92-4d9a-8c62-00a2c7fc8f78.png)


![image](https://user-images.githubusercontent.com/32221934/229387727-67010026-d62e-47d8-b9d8-536135a650b8.png)

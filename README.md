# Designing Database
 This project involves designing an oracle database for a hotel. The project spanned from brainstorming on the problem to creating an ERD diagram and writing DDL commands to implement it  


## Problem Statement

Hey there!
Here are the high-level details of the HOTEL RESERVATION system, process, and key data we need to be tracking.  
Objective: Below is an overview of a hotel reservation system.  Please review the processes below to gain an understanding of the organizational context for which we are designing this database 
 Background: The Sour Apple Hotel, a South Austin boutique hotel, acquired funding a year ago and has already begun expanding      its operations into a diverse set of properties. Not having a single source for storing its data, it is now ready to build a single centralized reservation system that will manage all its diverse locations, customers, and reservations. Presently, they’re managing each of their three locations’ data separately and having to merge it all in QuickBooks for accounting/reporting and this is not sustainable especially if they plan to keep expanding. Their current locations include their original hotel location on South Congress, the East 7th Lofts, and their cabins near the Balcones Canyonlands which are actually west of Austin in the city, Marble Falls. Like any other hotel, you can reserve a single room to stay or a “block” of rooms. Locations can share similar features like “Free Breakfast” but due to their diverse nature can have features unique to that specific location. The system you make should be able to handle all key data such as the various locations and the customer reservations of rooms at these locations. Once this database is built it will support internal operations, the plan will be to integrate it to their website to allow for online viewing of room features but also customer account setup and room reservations.

 Customer Account Signup process: When a new customer is reserving a room or checking in, the Sour Apple staff will set up an account for that person. This requires a first and last name, email, address, and a single phone number. This account is used to automatically track their stay credits earned. Each night stay (per room) earns a single credit. 10 credits can be redeemed for a free night’s stay in one room. The team tracks total credits earned and credits used to understand how many credits a person has left to use currently while retaining a simple history of how many they’ve earned in a lifetime. Each customer will have a single credit card on file since Sour Apple keeps things simple and doesn’t want to track multiple payments for customers.

 Room Reservation process: When a customer wants to make a reservation currently, it’s done by calling the location they want to stay with or making the reservation at the front desk of that location. Once Sour Apple has a centralized system, their      hope is that any location can take reservations for another location, or you can reserve rooms at any location online. When a customer requests a reservation their customer_id is tied to the reservation if it’s known. If it’s a new customer, staff creates a customer account first and then assigns the id. A check-in date and anticipated check-out date are captured and then a number of rooms is requested to figure out if there are enough rooms at the location to fulfill the reservation. If they can’t fulfill the reservation we won’t create it. If the customer has a discount code that can be applied to the reservation at that time otherwise it’s left blank. Once the reservation is created and the rooms are attached to it, a Confirmation number is randomly generated and stored on the reservation along with the date it was created. A single character status is also assigned to track what status the reservation is in (see more detail below on this). For each room on the reservation, the number of anticipated guests is logged since each room has a max capacity. After the stay, the customer is asked to provide a rating of 1 to 5 stars that can be captured and stored on the reservation if they complete the rating survey!
 
 # ERD Diagram
 ![image](https://user-images.githubusercontent.com/87246714/142699678-a6456f3d-ce36-44a1-b25d-ff5a19775b2b.png)


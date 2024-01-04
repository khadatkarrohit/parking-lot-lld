# Parking Lot LLD
The low-level architecture for a backend system of a smart parking lot. This system should handle vehicle entry and exit management, parking space allocation, and fee calculation.

# Project Requirements

1. The parking lot should have multiple floors where customers can park their cars.
2. The parking lot should have multiple entry and exit points.
3. Customers can collect a parking ticket from the entry points and can pay the parking fee at the exit points on their way out.
4. Customers can pay the tickets at the automated exit panel or to the parking attendant.
5. Customers can pay via both cash and credit cards.
6. Customers should also be able to pay the parking fee at the customer’s info portal on each floor. If the customer has paid at the info portal, they don’t have to pay at the exit.
7. The system should not allow more vehicles than the maximum capacity of the parking lot. If the parking is full, the system should be able to show a message at the entrance panel and on the parking display board on the ground floor.
8. Each parking floor will have many parking spots. The system should support multiple types of parking spots such as Compact, Large, Handicapped, Motorcycle, etc.
9. The Parking lot should have some parking spots specified for electric cars. These spots should have an electric panel through which customers can pay and charge their vehicles.
10. The system should support parking for different types of vehicles like car, truck, van, motorcycle, etc.
11. Each parking floor should have a display board showing any free parking spot for each spot type.

# Class Diagram
Here are the main classes of our Parking Lot System:

1. ParkingLot: The central part of the organization for which this software has been designed. It has attributes like ‘Name’ to distinguish it from any other parking lots and ‘Address’ to define its location.
2. ParkingFloor: The parking lot will have many parking floors.
3. ParkingSpot: Each parking floor will have many parking spots. Our system will support different parking spots 1) Handicapped, 2) Compact, 3) Large, 4) Motorcycle, and 5) Electric.
4. Account: We will have two types of accounts in the system: one for an Admin, and the other for a parking attendant.
5. Parking ticket: This class will encapsulate a parking ticket. Customers will take a ticket when they enter the parking lot.
6. Vehicle: Vehicles will be parked in the parking spots. Our system will support different types of vehicles 1) Car, 2) Truck, 3) Electric, 4) Van and 5) Motorcycle.
7. EntrancePanel and ExitPanel: EntrancePanel will print tickets, and ExitPanel will facilitate payment of the ticket fee.
8. Payment: This class will be responsible for making payments. The system will support credit card and cash transactions.
9. ParkingRate: This class will keep track of the hourly parking rates. It will specify a dollar amount for each hour. For example, for a two hour parking ticket, this class will define the cost for the first and the second hour.
10. ParkingDisplayBoard: Each parking floor will have a display board to show available parking spots for each spot type. This class will be responsible for displaying the latest availability of free parking spots to the customers.
11. ParkingAttendantPortal: This class will encapsulate all the operations that an attendant can perform, like scanning tickets and processing payments.
12. CustomerInfoPortal: This class will encapsulate the info portal that customers use to pay for the parking ticket. Once paid, the info portal will update the ticket to keep track of the payment.
13. ElectricPanel: Customers will use the electric panels to pay and charge their electric vehicles.
    

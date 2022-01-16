# CAB BOOKING APPLICATION

# Overview 
**Cabby** is yet another cab booking application with some added functionalities. It provides both inter- city as well as intra-city rides. This application has been built by keeping security as the paramount feature. Along with driver’s background verification checks, it also focus on customer’s background verification. Both the driver and customer have to provide a government ID as part of the registration process.  
It aims to provide maximum flexibility to users while booking a cab with the help of filters, like a female customer can choose a female cab driver if she wants, a cab of their choice like (SUV, Sedan, Hatchback,etc.) and many more.  
At the completion of trip, both customer and driver will provide a “star” rating to each other. This would contribute towards getting an overall score for the driver and user so that drivers and users can be matched accordingly for upcoming rides. **For Example** a customer with higher ratings would get matched to cab drivers who have high ratings.

# Important Features

## a. Registration and Sign-In 
### Customer Registration
Customers can simply register themselves by providing simple details like Name, date of birth, contact details, address, and ID proof. ID proofs will be a mandatory requirement and all details would be verified by the admin. After that, Customer will be eligible to use the application.
### Driver Registration
Registration workflow for driver will be slightly different wherein driver has to give some extra details like driving licence, number of years of experience,  car details, area where driver will operate etc. Once a driver submits the details, there will be a verification check performed by the Admin. After complete verification, driver will be marked as successfully registered on the application.
### Sign-In
There will be three sign-in options, one each for customer, driver, and admin. The respective person can login using username and password provided in the registration process. If someone forgets the password, they can choose to reset the password with the help of their email address for getting a password reset link.  
Below mentioned screnshot has the workflow of already registered Customer.

![image](https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/1.png)

## b. Cab Selection
Cab selection by Customer/Passenger is an essential component of this application. While booking a cab there are multiple points of screening starting from different cab types (sedan, SUV, XUV, premium sedan, etc).Some screening parameters in selection of cabs are:
- Distance of Cab from customer’s location.
- Traffic on a particular route (from user’s current location to cab’s current location).
- Gender preference from customer’s end. For example, a female candidate might prefer a female driver.  
    **Example of showing best available cab:**  
    **Scenario 1:** Cab 1 is 2 km away from user’s location, however, there is a lot of traffic in that route.  
    **Scenario 2:** Cab 2 is 3 km away from user’s location, however, there is no traffic in that route.    
    Considering the above scenario, this application will book Cab 2 as it will reach faster at user’s current location.  
- Upon fetching most nearby cabs, customer will further have an option of screening on parameters like gender, age, ratings etc.

**The Concept of Number Line is used to Calculate distance between Source and Destination**
![image](https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/Flowdiagram.png)
Steps in booking cab:  
a. Choose Cab Type (sedan, SUV, XUV, premium sedan, etc).  
b. Add Source and Destination Locations.  
c. After giving source and destination our application will fetch nearby cabs from source location. Cabs within 5 Km range will be fetched.   
d. Application will find best cabs from list of nearby cabs based on Traffic density and Distance Parameters    
**Traffic feature has below mentioned values:**
- Low Traffic : Speed = 50 km/hr
- Moderate Traffic : Speed = 40 km/hr
- High Traffic : Speed = 30 km/hr  

Based on Speed and Distance we are calculating the Approximate Time which each nearby cab will take.
<table>
  <tr>
    <td>a.</td>
    <td>b.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/1.png" width=470 height=400></td>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/2.png" width=470 height=400></td>
  </tr>
   <tr>
    <td>c.</td>
    <td>d.</td>
  </tr>
   <tr>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/3.png" width=470 height=400></td>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/4.png" width=470 height=400></td>
  </tr>
 </table>

## c. Price Calculation for each Ride
There are several factors on which this application calculates fare of the ride:
- Distance between source and destination (For every ride fixed ‘x’ dollars are charged for first 3 kms and thereafter ‘y’ dollars per km. Additional 25% charge  on fixed rates for night rides between 11:00 pm to 5:00 am).
- Time taken to complete the distance (Fixed ‘z’ dollars/cents are charged per minute throughout the journey).
c. Time of booking rides. (If someone books ride during peak hours like office hours than price of booking will increase by 20% as demand of cabs at peak hours is higher).
- Location of the traveller. (For metro cities prices would be bit higher as compared to countryside areas)
- If a passenger prefer to share their ride with Co-passenger than total fare is reduced by ‘x’ percent).
- If a passenger wants Internet and Car TV during ride (Fare increases by fixed ‘x’ dollars for a specific time interval. For example, $2 is charged extra per 30 minutes of ride).
![image](https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/4.png)

## d. Income of Cab Driver
The drivers can check their earnings using this feature. Below are the parameters that will affect the earnings:
1. Total Rides  
2. Incentives based on – number of rides, number of kilometres, number of hours etc.  
The Driver pays a commission to the company based on completed rides. There will be a daily target that can add incentives which will help to componsate the commission. Suppose company is taking 20% commission, the drivers will pay less commission to the company if they complete any one of the following targets:
- Completed specified number of rides.
- Completed specified number of kilometres.
- Completed specified number of hours on one ride.

**Logic for Calculating Commission**
![image](https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/5.png)

<table>
  <tr>
    <td>a.</td>
    <td>b.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/6.png" width=470 height=400></td>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/7.png" width=470 height=400></td>
  </tr>
 </table>

## e. List of Rides 
The user will be able to see the list of completed rides. This feature will have the below options to see the list of rides:
1. Daily  
2. Monthly  
3. Select a period  
The user can select the option “Show Rides” after logging into the system. The system will check the rides in the database for the specified period and will display the result.
<table>
  <tr>
    <td>a.</td>
    <td>b.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/8.png" width=470 height=400></td>
    <td><img src="https://github.com/ManjinderSingh3/Cab-Booking-Application/blob/master/outputs/9.png" width=470 height=400></td>
  </tr>
 </table>

## f. Star Ratings and Score
Every driver and Customer are non-rated and non-scored upon registering. Both of them are given 10 rides to get familiar with the rating and scoring process. Upon finishing first 10 rides they are given an initial **rating** and **score** of 4.0 out of 5.0.  
Maintaining their overall score is totally dependent upon themselves. The drivers and the customers have an option of giving each other a **star** rating out of 5 after every ride based on the overall experience. The overall star rating is the average number of stars received after every ride. Also, these star ratings affect the overall score.  

**The scoring process:**
### i. For Driver
Arrival/Drop before the last minute of estimated time: +0.2  
Arrival/Drop within the last minute of estimated time: +0.1  
Arrival/Drop after the estimated time: -0.1 for every additional 2 minutes 5-star rating from the user: +0.3  
4-star rating from the user: +0.1  
3-star rating from the user: -0.1  
2-star rating from the user: -0.3  
1-star rating from the user: -0.5  
Cancellation after accepting the ride and before reaching the pick-up point: -0.1 Cancellation after accepting the ride and reaching the pick-up point: -0.5  
### ii. For Customer
Boarding the cab within 1 minute of its arrival: +0.2  
Boarding the cab within 1-2 minutes of its arrival: +0.1  
Boarding the cab after 2 minutes of its arrival: -0.1 for every additional minute 5-star rating from the driver: +0.3  
4-star rating from the driver: +0.1  
3-star rating from the driver: -0.1  
2-star rating from the driver: -0.3  
1-star rating from the driver: -0.5  
Cancellation after driver’s arrival: -0.5  
Cancellation before driver’s arrival: -0.2  
Cancellation within 1 minute of booking the ride: -0.1  

# How to run code locally 🛠️

- Before following below mentioned steps please make sure you have [git](https://git-scm.com/download) and [java](https://www.oracle.com/java/technologies/downloads/) installed on your system. 
- Clone the complete project with `git clone https://github.com/ManjinderSingh3/Cab-Booking-Application.git` or you can just download the code and unzip it.
- After cloning this project, perform below mentioned steps in command line:  
  - ```mvn clean compile```
  - ```mvn clean test```
- Now, finally run dummy application from this path
  - ```java src/main/java/com/dal/cabby/Application.java``` 
- Also you can executable jar file which is created in the target folder.
- The command to execute Jar file is
  - ```java -jar target/cabby-1.0-jar-with-dependencies.jar```


## Group Members:

* MANJINDER SINGH 
* DEVRAJ SINGH
* BIKRAMJIT SINGH 
* MANRAJ SINGH 
* ARVINDER SINGH  

# Contact 📞
#### If you have any doubt or want to contribute to this project feel free to email me or drop your message on [LinkedIn](https://www.linkedin.com/in/manjinder-singh-a23aa3149/)

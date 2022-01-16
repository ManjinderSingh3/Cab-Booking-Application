# CAB BOOKING APPLICATION

# Overview 
**Cabby** is yet another cab booking application with some added functionalities. It provides both inter- city as well as intra-city rides. This application has been built by keeping security as the paramount feature. Along with driver’s background verification checks, it also focus on customer’s background verification. Both the driver and customer have to provide a government ID as part of the registration process.  
It aims to provide maximum flexibility to users while booking a cab with the help of filters, like a female customer can choose a female cab driver if she wants, a cab of their choice like (SUV, Sedan, Hatchback,etc.) and many more.  
At the completion of trip, both customer and driver will provide a “star” rating to each other. This would contribute towards getting an overall score for the driver and user so that drivers and users can be matched accordingly for upcoming rides. **For Example** a customer with higher ratings would get matched to cab drivers who have high ratings.

# Important Features

## a. Registration and Sign-In 

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


## c. Price Calculation for each Ride
There are several factors on which this application calculates fare of the ride:
- Distance between source and destination (For every ride fixed ‘x’ dollars are charged for first 3 kms and thereafter ‘y’ dollars per km. Additional 25% charge  on fixed rates for night rides between 11:00 pm to 5:00 am).
- Time taken to complete the distance (Fixed ‘z’ dollars/cents are charged per minute throughout the journey).
c. Time of booking rides. (If someone books ride during peak hours like office hours than price of booking will increase by 20% as demand of cabs at peak hours is higher).
- Location of the traveller. (For metro cities prices would be bit higher as compared to countryside areas)
- If a passenger prefer to share their ride with Co-passenger than total fare is reduced by ‘x’ percent).
- If a passenger wants Internet and Car TV during ride (Fare increases by fixed ‘x’ dollars for a specific time interval. For example, $2 is charged extra per 30 minutes of ride).

## d. Income of Cab Driver

## e. List of Rides 

## f. Star Ratings and Score

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

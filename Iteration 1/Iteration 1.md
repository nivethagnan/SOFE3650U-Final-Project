# Iteration 1: Establishing an Overall System Structure

Iteration 1 report pdf can be viewed [here]()

## Step 1: Review Inputs

In this step of the ADD method, we will review the inputs and show which requirements will be the drivers, as shown below. 

| Categories | Details |
| --- | --- |
| Design Purpose | The purpose is to produce a detailed design to allow the construction of the application in the most efficient manner |
| Primary Functional requirements | The primary use cases we will be using will be the following: UC-1: Monitoring the Network Status, UC-2: Detecting Faults in the Network, UC-8: Displaying information, UC-10: User Authentication |
| Quality Attribute Scenarios |![Screenshot (294)](https://user-images.githubusercontent.com/80362439/144941781-92ad6d9b-498e-45a6-908f-916898268b9f.png) |

## Step 2: Establish Iteration Goal by Selecting Drivers

* QA-1: Performance
* QA-3: Modifiability
* QA-4: Security
* QA-5: Interoperability
* QA-6: Availability
* CON-2: Application must be accessible to the public. This cannot interfere with existing users’ security information
* CON-3: Decreased bandwidth for user convenience without affecting overall performance
* CRN-2: App suitable for customers across all devices

## Step 3: Choose One or More Elements of the System to Refine

![unnamed (1)](https://user-images.githubusercontent.com/80362439/144941893-8aae7472-46eb-4c21-8328-b4a58740f17c.png)

## Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers

| Design Decisions and Locations | Rationale | Discarded alternatives: |
| --- | --- | --- |
| Logically using the SmartShop Request  using the Mobile Application reference architecture  | The reference architecture (see Section A.1.4) supports the development of the SmartShop application being installed on customer and store devices. This allows the user to have an enjoyable UI experience and have adequate performance  (UC-1) . These capabilities are also helpful in achieving QA-2. This application is not suited for a web browser, as explained in CON-1. They would need to be installed via the app store. | Web Applications: The reference architecture is oriented towards the development of applications that are accessed from a web browser. |
| Physically structure the application using the three-tier deployment program | Because the application must be accessed from a mobile application (CON-1), and the existing database (CON-4) will be here to support the SmartShop system, so a three tier system can be used to be deployed. | |
| Logically structure the Request Server using the Service Application reference architecture | Service applications won’t be providing the user interface any benefits, but will allow the app to function whilst being closed so orders won’t get cancelled even if you close the app. | |
| Build the user interface of the client using Swift | The standard framework for building applications using Swift ensures portability (CON-3) and the developers are most familiar with. (CRN-2) | |

## Step 5:  Instantiate Architectural  Elements, Allocate  Responsibilities, and Define Interfaces

| Design Decisions and Locations | Rationale |
| --- | --- |
| Remove local data sources in the Mobile Application reference architecture | With the network connection being reliable, SmartShop no longer needs to store data locally. Main communication with the server is controlled in the data layer and any other communication will be managed through local method calls |
| Deploy a data, application and user tier for the mobile application system | In the SmartShop system, the three-tier architecture used are data, application and user. The application and user tier is where the customer’s data is processed, and the data tier is where the data is stored and managed. |
| Implement a module dedicated to deploying data in the Service application reference architecture | Ensures user’s will still be receiving information/notifications regarding their orders even if they closed the app. This will further facilitate the achievement of QA-3. |

## Step 6: Sketch views and Record Design Decisions 
## Step 7: Perform Analysis of Current Design and Review Iteration Goal


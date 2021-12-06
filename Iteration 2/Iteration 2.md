# Iteration 2: Identifying Structures to Support Primary Functionality

Iteration 2 report pdf can be viewed [here](https://github.com/nivethagnan/SOFE3650U-Final-Project/blob/main/Iteration%202/Iteration%202.pdf)

## Step 2: Establish Iteration Goal by Selecting Drivers

The goal of this iteration is to address the concern of identifying structures and to support the primary functions:

UC-1: Monitor App Status 
UC-2: User Authentication
UC-13: Register

## Step 3: Choose One or More Elements of the System to Refine

The elements of the system that will be refined are display order history, we will be refining this element to display order history from a longer period of time.

## Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers

| Design Decisions and Locations | Rationale and Assumptions |
| --- | --- |
| Create a Domain Model for the application | We must identify the major entities in the domain along with their relationships. In order to do this we must create a domain model for the system. |
| Identify Domain Objects that map to functional requirements | We do this to each distinct functional element so we can understand the modules in different layers rather than have them all be coagulated. |
| Map the system use cases to domain objects | We use this to identify major entities so it can be analyzed and deciphered with whatever use cases the system has. |
| Use Spring framework and Hibernate | Spring because of how widely it is used, we can use it in our SmartShop for the application development. Hibernate also works very well with Spring. The development team also agrees that Spring is a good framework to work with. |

## Step 5: Instantiate Architectural  Elements, Allocate  Responsibilities, and Define Interfaces

| Design Decisions and Locations | Rationale and Assumptions |
| --- | --- |
| Create only an initial domain model | The primary use cases need to be outlined and defined but only in an initial domain model. |
| Map the system use case | We need to identify the objects that are all in our system use cases. |
| Associate frameworks with a module in the data layer | As spoken about earlier, we will be using the Spring and Hibernate framework hand in hand and in doing so we will be able to discuss previous modules. |
| Decompose the domain objects across the layers to identify layer-specific modules with an explicit interface | This will ensure that all the modules are being supported and all the functionalities will be identified. Making sure that it follows CRN-3, where all the concerns are that the server load will be divided of busy to non busy across different time zones. |

## Step 6: Sketch Views and Record Design Decisions 
![iteration 2 figure 1](https://user-images.githubusercontent.com/80362439/144938796-1e8e8238-d453-425d-9ece-3e3a93a30d1d.png)



## Step 7: Perform Analysis of Current Design and Review Iteration Goal


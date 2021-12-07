# Iteration 3: Addressing Quality Attribute Scenario Driver (QA-6)

Iteration 3 report pdf can be viewed [here](https://github.com/nivethagnan/SOFE3650U-Final-Project/blob/main/Iteration%203/Iteration%203.pdf)

## Step 2: Establish Iteration Goal by Selecting Drivers

QA-6  quality  attribute  scenario: 
A glitch can occur in the server database not processing any potential payment. The server will fix itself upon terminating the order and the application and then reopening it to clear cache, or will repair itself within 30 seconds.

## Step 3: Choose One or More Elements of the System to Refine

The elements of the system that we will refine are application server and the database server. 

## Step 4: Choose One or More Design Concepts That Satisfy the Selected Drivers

| Design Decisions and Location | Rationale and Assumptions |
| --- | --- |
| Introducing the active redundancy tactic by replicating the application server | By replicating the critical elements, the system can withstand the failure of one of the  replicated elements. This can be done without affecting other parts of the system. |
| Introduce an element from the Market queue | Traps received are placed in the market queue and then retrieved by the application.  |

## Step 5:  Instantiate Architectural  Elements, Allocate  Responsibilities, and Define Interfaces

| Design Decisions and Location | Rationale and Assumptions |
| --- | --- |
| Deploy market queue on  a separate node | Deploying the market queue on a separate node will guarantee that no traps are lost in case of application failure. |
| Use active redundancy and load balancing in  the application server | Because two replicas of the application server are active at any time,  it makes sense to distribute and balance the load among the replicas. |
| Implement load balancing and redundancy using technology support | Many technological options for load balancing and redundancy can  be  implemented without having to develop an solution that would be less mature and harder to support. |

## Step 6: Sketch views and Record Design Decisions 

![Figure 1 Refined deployment diagram](https://user-images.githubusercontent.com/80362439/144946162-024a11cf-c80a-41ff-90ff-6201d854274c.png)
Figure 1: Refined deployment diagram

![Figure 2 Sequence diagram](https://user-images.githubusercontent.com/80362439/144946174-510fc2ef-abdf-4be8-a5a8-f4c3a695fef0.png)
Figure 2: Sequence Diagram

## Step 7: Perform Analysis of Current Design and Review Iteration Goal

The design decisions made in this iteration impacted QA-3 and QA-1, understanding of the efficiency and functionality and how it is used through the system. Drivers that were addressed in iteration 1 and 2 were not repeated in this table.

| Not Addressed | Partially Addressed | Completely Addressed | Design Decisiosn made during this Iteration | 
| --- | --- | --- | --- |
| | | QA-1 | A main separate node that was used in this iteration helped separate the servers preventing failures in the application. |
| | QA-2 | | No decisions made |
| | QA-3 | | The node used along with the receiver/balancer makes sure there are no possibility of failures in the system. |
| | QA-4 | | No decisions made |
| | CON-1 | | Receiver and balancer with the different servers will ensure that different user requests are dealt with in a better manner. |
| | CON-2 | | No decisions made |
| | CON-4 | | No decisions made |
| | CON-5 | | No decisions made |
| | CON-6 | | No decisions made |



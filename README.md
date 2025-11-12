# INVENTORY AND SUPPLY CHAIN MANAGEMENT
## PL/SQL Collections, Records, and GOTO Statements
**Student Name:** Ngabo Tresor

**Student ID:** 27209
## Problem Definition
A large retail company needs an efficient, automated system to manage product inventory across multiple warehouses. The system must process incoming shipments, track stock levels, calculate reorder points, classify products based on velocity, and flag critical stock shortages.

## Goal
1.Systematically log and manipulate diverse product characteristics (location, volume, cost details).

2.Determine asset financial worth and establish the typical replenishment lead time.

3.Group inventory items according to their rate of turnover (e.g., High/Medium/Low velocity tiering).

4.Pinpoint severely depleted items that require the immediate issuance of procurement directives.

5.Produce comprehensive validation reports for warehouse supervisors and the acquisitions team.o

## Encountered Setbacks
1.Managing diverse data entities (products, vendors, transactional logs, supply figures).

2.Efficiently manipulating large sets of correlated stock records and their relationships.

3.Managing abnormal conditions and data inconsistencies (e.g., zero count, negative valuation, damaged goods).


## The operations of the database
The database serves as the foundational data layer for the Asset Tracking and Logistics Oversight system. It is composed of three interconnected tables designed to separate static product data from dynamic inventory levels and process exceptions.

Products stores the master attributes (e.g., cost, reorder point) for every item.

Inventory_Stock holds the real-time, current stock levels that the PL/SQL processing block reads.

Audit_Log acts as the crucial transaction history, recording when the emergency GOTO routine is triggered.

This structure ensures data integrity, provides the necessary data input for the Collections and Records processing, and validates the execution of the critical GOTO control flow logic.
# Screenshots

The Creation of Tables.

<img width="559" height="411" alt="table creation" src="https://github.com/user-attachments/assets/616b876d-ebf3-436b-86aa-6a6bec2c6dbd" />

The Insertion of Rows.

<img width="856" height="341" alt="data insertion 1" src="https://github.com/user-attachments/assets/5f4eefd4-f9ab-487c-8f70-8da5746f6a04" />
<img width="715" height="207" alt="data insertion" src="https://github.com/user-attachments/assets/905672e7-4805-4645-b4c0-0b34ecf39fff" />


The Output of Data.

<img width="510" height="428" alt="Capture1" src="https://github.com/user-attachments/assets/ec30c782-0103-4535-84d8-1c2123cc9834" />
<img width="504" height="468" alt="Capture" src="https://github.com/user-attachments/assets/7baabb97-5aaf-4c0c-a229-cbc2abaae2c0" />


The Functionality and Efficiency of The procedure.




<img width="385" height="175" alt="result" src="https://github.com/user-attachments/assets/8a6c723d-cfe8-4f2d-883e-b1768f6433eb" />
<img width="446" height="190" alt="result1" src="https://github.com/user-attachments/assets/341fb834-16c1-4397-956d-3ac7e9d8ea7e" />




The procedure is highly efficient because its main function is to enforce immediate action on critical shortages.

It uses a Collection of Records for batch processing. The moment Product 4003 is checked and found critically low, the GOTO statement interrupts the routine. This instantly skips any remaining non-critical work and logs the emergency to the database, ensuring the fastest possible response time for the supply chain issue
# Conclusion
Record: The r_inventory_item Record was used to define a single, complex product structure (Stock, Cost, Reorder Point), ensuring accurate value calculation during processing.

Collection: The t_inventory_batch Collection (Index-by Table) efficiently stored and allowed for the quick, iterative checking of all inventory records in memory.

GOTO Statement: The GOTO statement was critical for enforcing Emergency Priority. When a critical stock shortage was detected, it immediately halted the normal routine and redirected control to the Procurement Routine, skipping unnecessary subsequent checks.



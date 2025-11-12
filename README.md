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

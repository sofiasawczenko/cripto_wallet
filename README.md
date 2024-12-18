# **Title: _Cryptocurrency Investment System_**

## **Table of Contents**

[Introduction 3](#_Toc169438809)  
[Target Audience 3](#_Toc169438810)  
[PO's Pain Points 3](#_Toc169438811)  
[Proposed Solution 3](#_Toc169438812)  
[System Modeling 3](#_Toc169438813)  
[1. Database Modeling 3](#_Toc169438814)  
[2. Backend Modeling 4](#_Toc169438815)  
[System Infrastructure 6](#_Toc169438816)  
[1. Physical Topology 6](#_Toc169438817)  
[2. Logical Topology 7](#_Toc169438818)

---

## **Introduction**

The project aims to develop a software system that allows the Product Owner (PO), Uncle Scrooge, to invest in cryptocurrency assets securely, efficiently, and accessibly via the web. This document describes the product scope, target audience, identified pain points, and the proposed solution.

## Target Audience

- Individual and corporate investors interested in cryptocurrency assets.
- Users who prefer to access their investments via the web.
- Individuals concerned with the security of their financial data.

## PO's Pain Points

1. The need to invest in cryptocurrency assets online.
2. Daily tracking of investments.
3. Data and value security during network transmission.
4. Transfers between multiple companies.
5. Preference for accessing and making investments via a web system.

## Proposed Solution

- Invest in cryptocurrency assets securely and efficiently.
- Track investments daily through detailed reports.
- Ensure data security with two-factor authentication and encryption.
- Make transfers between different accounts.
- Enjoy an intuitive and responsive interface.

## System Modeling

### Database Modeling

Database modeling is critical to ensure system performance and integrity. The Entity-Relationship model below describes the entities, their attributes, and the relationships between them.

### Backend Modeling

Backend modeling is essential to ensure the cryptocurrency investment system is robust, scalable, and maintains data integrity. The following class diagram describes the structure of backend classes, including their responsibilities, attributes, and methods. Each class has been carefully designed to reflect the system’s main operations and entities, promoting a clean and modular architecture.

Note: The high-definition image was sent in the same zip file under the name "Class Diagram.png".

The class model consists of the following parts:

**Main Entities:**

- **User:** Represents system users, storing information such as ID, name, email, password, and creation date.
- **Account:** Represents users' investment accounts, linking each account to a user and cryptocurrency type, as well as maintaining the balance and account number.
- **Transaction:** An abstract class that serves as the base for various transaction types like deposits, withdrawals, and transfers, storing common transaction information.
- **Deposit:** An extension of the Transaction class, representing a deposit made into an account.
- **Withdrawal:** An extension of the Transaction class, representing a withdrawal from an account, including balance validation.
- **Transfer:** An extension of the Transaction class, representing a transfer between two accounts, including source and destination accounts.

**Services:**

- **AccountService:** Provides essential account operations such as login, deposit, withdrawal, and transfer, applying specific business rules to each operation.

**Repositories:**

- **UserRepository:** Manages user data access, including search and save operations.
- **AccountRepository:** Manages account data access, including search and save operations.
- **TransactionRepository:** Manages transaction data access, including search and save operations.

The class diagram illustrates how these parts interact, ensuring the system can meet security, efficiency, and functionality requirements, providing a solid foundation for backend development.

## System Infrastructure

### Physical Topology

- **Application Servers:**
  - **Web Server:** Hosts the web application where users access the system.
  - **API Server:** Manages API requests, facilitating communication between the frontend and backend.
  - **Application Server:** Processes business logic, including deposit, withdrawal, transfer operations, and currency price updates.
  
- **Database Servers:**
  - **Primary Database:** Stores critical data such as users, accounts, and transactions.
  - **Backup Database:** Replicates all data from the primary database, ensuring redundancy and recovery in case of failure.

- **Security Servers:**
  - **Firewall:** Protects the network from unauthorized access.
  - **Authentication Server:** Manages user authentication, including two-factor authentication (2FA).

- **Monitoring Servers:**
  - Monitors server performance, detects failures, and ensures preventive maintenance.

- **Backup and Recovery Servers:**
  - Performs regular data and application backups, ensuring fast recovery in case of failure.

### Logical Topology

- **Presentation Layer:**
  - **Frontend:** Web interface where users interact with the system.
  - **API Gateway:** API interface that serves as the entry point for all frontend requests.

- **Application Layer:**
  - **Application Services:** Backend components that process business logic, such as withdrawal, deposit, transfer operations, and cryptocurrency price updates.
  - **Authentication Services:** Manage user authentication and authorization.

- **Data Layer:**
  - **Database Services:** Manage access to stored data, including queries, inserts, updates, and deletions.
  - **Backup Services:** Manage data replication and backup.

- **Security Layer:**
  - **Firewall Services:** Protect the system from unauthorized access and attacks.
  - **Encryption Services:** Ensure sensitive data is transmitted securely.

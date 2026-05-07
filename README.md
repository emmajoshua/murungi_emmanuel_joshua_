THE LINK BELOW IS THE ONE TO MY PRESENTATION VIDEO 
https://drive.google.com/file/d/1Cla-YBZ2x5nyU61iF0Zt-hvNHL1ktuK2/view?usp=sharing
and this is the link to youtube 
https://youtu.be/0RvjIo8b3GA
This README file is based on the technical documentation for the **Banking Customer Details Management System (BCDMS)**, a project designed for the Database Systems course at Mbarara University of Science and Technology[cite: 95, 102].

 Banking Customer Details Management System (BCDMS)

 1. Project Overview
[cite_start]The **Banking Customer Details Management System (BCDMS) is a specialized sub-system designed to manage the full lifecycle of customer data—from initial onboarding and Know Your Customer (KYC) capture to account linkage[cite: 107]. [cite_start]This project was developed to address the fragmentation issues often found in small-to-medium financial institutions (such as SACCOs) that rely on manual or spreadsheet-based records[cite: 108, 109].

[cite_start]Built on a centralized MySQL relational database, the system is inspired by industry-standard solutions like the Finacle Core Banking System[cite: 109].

 2. Key Features
 Unified Customer Profiles: Creates a "golden record" for every customer, linking their personal details to all associated bank accounts[cite: 112].
 [cite_start] Data Integrity:Implements strict referential integrity rules to ensure no "orphaned" records (e.g., an account cannot exist without a valid customer)[cite: 150, 165].
 [cite_start] Efficiency: Reduces customer onboarding time from 45 minutes to approximately 10 minutes[cite: 129].
  [cite_start] Role-Based Access Control: Defines specific data access for different user groups including Tellers, CRM Managers, Compliance Officers, and IT Administrators[cite: 118].
 [cite_start] Soft-Delete Pattern:Closed accounts are marked as "Inactive" rather than being deleted to preserve a complete audit trail[cite: 125, 287].

3. Database Architecture
[cite_start]The system utilizes a normalized relational structure (adhering to **3NF**) to eliminate redundancy and ensure scalability[cite: 152, 250].

    Core Schema (6 Tables)
1.  [cite_start]`customer_bio`: Primary table for identity data (Names, DOB, Gender, Email)[cite: 145, 168].
2.  [cite_start] `account_details`: Stores financial attributes (Account Number, Balance, Account Type, Status)[cite: 146, 170].
3.  [cite_start]`customer_contact`: Links to `customer_bio` (1:1) for phone numbers and addresses[cite: 172].
4.  [cite_start]`loan_records`: Tracks various loan products issued to a customer (1:M)[cite: 174, 175].
5.  [cite_start]`transaction_history`: A dynamic ledger recording every deposit and withdrawal (1:M)[cite: 176, 177].
6.  [cite_start]`branch_details`: Manages information regarding the physical branch network[cite: 178, 179].


  Technical Highlights
 [cite_start]`DECIMAL(15,2)`: Used for balances to ensure exact financial precision and avoid rounding errors common with floating-point types[cite: 160, 283].
 [cite_start]`ENUM` types: Used for gender and account types to enforce a controlled vocabulary and prevent data entry inconsistencies[cite: 161, 276].
 [cite_start]Composite IDs: `customer_id` uses a formatted string (e.g., `CID-2024-1001`) to include registration years for better auditability[cite: 273].

   4. Sample Queries
The system supports advanced SQL analytics for management intelligence:
 [cite_start] High-Value Customer Identification: Filtering active accounts with balances exceeding specific thresholds[cite: 305, 306].
 [cite_start] Demographic Analytics: Grouping data by gender or age to understand customer distribution[cite: 310].
 [cite_start] Operational Views: Creating specific "Teller Views" that hide sensitive information like addresses or dates of birth to enhance security[cite: 61].

   5. Development Details
 [cite_start]**Developer:** Murungi Emmanuel Joshua [cite: 100]
 [cite_start]**Institution:** Mbarara University of Science and Technology [cite: 95]
 [cite_start]**Reg Number:** 2025/BCS/128/PS [cite: 101]
 [cite_start]**Date:** May 2025 [cite: 104]

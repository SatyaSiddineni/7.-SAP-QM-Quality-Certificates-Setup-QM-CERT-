SAP QM Quality Certificates


1. Project Overview

            Quality Certificates in SAP QM (QM-CERT) are used to generate and manage certificates of analysis, inspection certificates that are sent to customers or received from vendors. These certificates ensure transparency of quality results and compliance with contractual and regulatory requirements.

            This project explains the end-to-end Quality Certificate setup, configuration steps, business process flow, and test data from an SAP QM Functional Consultant perspective.


2. Business Scenario

            Customer requires a Certificate of Analysis (CoA) with every delivery
            Certificate must include inspection results from inspection lot
            Certificate should be generated automatically at delivery or manually when required


3. Process Flow

            Sales Order / Goods Receipt
                        ↓
            Create Inspection Lot (Automatic)
                        ↓
            Record Inspection Results (QE51N)
                        ↓
            Usage Decision (QA11)
                     ↙ Yes                         ↘ No
               Generate Certificate         Reject / Rework
                    (QC20 / QC21)
                        ↓
               Send Certificate to Customer
                    (Print / Email / PDF)
                        ↓
               Archive Certificate in SAP


5. SAP Transaction Codes Used
   
            T-Code	          Purpose
            QS21	          Create Inspection Plan
            QE51N	          Results Recording
            QA11	          Usage Decision
            QC20	          Certificate Processing
            QC21	          Display Certificate
            VL01N	          Create Delivery


6. Project Structure

            SAP-QM-QM-CERT/
            │   
            ├── README.md
            ├── Documents/
            │     └── SAP QM CERT Documentation.pdf     
            │
            ├── Flowchart/
            │     └── QM CERT Process Flow.png
            │
            └── Test_Data/
                  └── SAP QM CERT Test Data.xlsx
         

🙌 Author

Satyanarayana Siddineni SAP Functional Consultant


---
layout: default
title: Vendor Reconciliation for Business Central
description: Support and documentation for Braintree's Vendor Reconciliation extension to Microsoft Dynamics 365 Business Central
---

## The business challenge
As a business, we procure products and services from external suppliers. The supplier maintains a record of what they have supplied to our business, and issues invoices to us. Based on the invoices, the supplier makes claims for payment.  We also maintain records of what we have procured from the suppliers, what they have delivered and what we agreed to pay for services. In theory, our records and the supplier's records should match, but often they do not. This can happen for a number of reasons, for example
* Timing differences: the supplier has raised a valid invoice on their statement, but we have not yet processed it on our system.
* Documents missing: an invoice may not have reached us, or got lost.
* Human error: the supplier may have billed us in error for something that was not delivered, or we may have accidentally captured an invoice to the wrong supplier account.
* We may have made a payment which they have not captured on their system.

Additionally, we may have disputes with a supplier about quantities, quality or price. Before we reach agreement on what should be paid, we need to record and resolve the disputes.

The Procure-to-Pay process is susceptible to fraud, theft and abuse in many businesses, and therefore requires oversight. It is an area which auditors pay significant attention to. Well-defined and disciplined processes in this business area contribute to having clean audits and high confidence levels from stakeholders.
 
## What is a Vendor Reconciliation?
The Vendor Reconciliation is a part of the Procure-to-Pay process in the supplier-customer relationship. As a business, it allows us to
* confirm that invoices presented by suppliers are valid charges for goods and services provided to the business
* compare the suppliers' claims for payment against our own record of what is due 
* base our decision of how much to pay to each supplier on objective facts.

The process is typically performed at least once a month for each active supplier, by an Accounts Payable administrator.

## Why every business should perform the vendor reconciliation process 
* It's important to have an accurate picture of what is owed to each supplier.
* We need to make fair decisions on what to pay a supplier for their services. 
* We need to manage disputes and discrepancies.
* We need to provide visibility on our creditors' liability for stakeholders - shareholders, directors, auditors, banks, and the creditors themselves.

## How to do a vendor reconciliation
* Extract the unsettled invoices for the supplier from our creditors ledger
* Using the creditor's statement, tick off the transactions which match our ledger - where the document number and amount on the statement matches exactly with the external document number and amount in our ledger.
* Identify transactions appearing on the creditors statement, which are missing from our ledger. Mark these as reconciling items on the statement.
* Identify transactions appearing on our ledger, which are missing from the creditors statement. Mark these as reconciling items on our ledger.
* Identify transactions which appear on the statement and the ledger, but amounts differ.
* Create a reconciliation of the amount owing:
  * Creditor balance as per our ledger
  * Plus documents on statement missing from our ledger
  * Minus documents our ledger missing from the statement
  * Plus the difference on transactions between ledger and statement
* For the transactions which match, record any applicable deductions, for example rebates, or due to disputes.
* Calculate the amount owing for matching documents, less deductions
* Process a payment to the creditor.

## The Braintree Vendor Reconciliation for Business Central
Instead of performing reconciliations manually, or on Excel, you can make use of the Vendor Reconciliation module of Business Central. This allows you to record the supplier's statement on the system, against your ledger entries.

After matching the creditors statement transactions against the business’s records, you can 
* Make a decision on the amount to be paid to the creditor
* Make deductions from the payable balance – for example, to cover damages, recover rebates etc.
* Process a payment to the creditor
* Print a remittance advice, detailing the transactions being settled
* Print a reconciliation between the balance stated by the creditor and the balance as per the business’s creditors ledger.

## Process Overview

   ![alt text](VRS_Process.drawio.svg)

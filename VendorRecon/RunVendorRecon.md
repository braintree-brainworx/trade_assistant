---
layout: default
title: Vendor Reconciliation for Business Central
description: Support and documentation for Braintree's Vendor Reconciliation extension to Microsoft Dynamics 365 Business Central
---
# Run Vendor Reconciliation

## Content
- [Start a new recon](#start-a-new-vendor-recon)
- [Load transactions](#load-transactions)
- [Reconcile Transactions](#reconcile-transactions)
- [Handling Settlement Discounts](#handling-settlement-discounts)
- [Capture Deductions](#capture-deductions)
- [Calculate payments](#calculate-the-payment)
- [Find a document](#find-a-document)
  
Search for 'Vendor Recon', and select the page. 
It's a good idea to bookmark this page.

The vendor recon list page will be displayed, showing active recons. The page includes preset views, based on the document status. By default, archived reconciliations are not displayed.

![alt text](ReconFilter.png)

If you do not see the Views list, open the Filter panel for the page.

## Start a new Vendor Recon
From the list page, click on New to open the recon page

![alt text](VendorReconCard.png)

- Tab off the No. field. A document number will be assigned. Date fields and batch fields will be initialised.
- Select the vendor. The vendor name, currency and statement number will be assigned

## Load transactions
The transactions to be matched come from two sources:
- Internal – entries recorded against the vendor’s account via normal procurement processes.
- External – entries presented by the vendor as due for payment. 

There are multiple methods to load entries due for payment:
- Internal entries will typically be loaded by importing them from the system. Transactions that have been previously settled will be inserted into the reconciliation.
- External entries can be captured manually, or imported from a spreadsheet template.

### Load Internal Transactions
Click on ‘Suggest Lines’ from the Statements menu:

![alt text](SuggestLines.png)

This will create an entry for each transaction on the vendor’s account which is due on or before the statement date, and which has not been previously settled. The following fields will be populated:

- Document date
- Document type
- Document no. (internal document number)
- External document number.
- Due date
- Ledger amount in original and local currency.
- Remaining amount in original and local currency.

### Option 1: Load Vendor Statement manually
- Update the recon header.
    - If necessary, amend the statement date to reflect the date on the vendor’s document.
    - Capture the total of the vendor’s statement in the field ‘Closing balance per statement’.
- Capture the transactions listed in the vendor statement.
    - If the recon contains a line loaded from the system, locate the entry and capture the value of the transaction as per the statement, into the field ‘Statement Amount’. Alternatively, tick the field ‘Match’ – the ledger amount will be automatically inserted into the Statement amount.
    - Transactions that are on the vendor statement, but are not recorded in the system, can be loaded by capturing the following details:
      - Document date
      - Document type
      - External document number
      - Due date
      - Statement amount.

### Option 2: Import from Excel
- Create an Excel template:
  - From the Statement menu on the reconciliation, click on ‘Import / Export’.
  - Select ‘Export Template’.

![alt text](ExportTemplate.png)

  - Open the Excel file that has been downloaded.
  - Capture the entries from the vendor’s statement onto the sheet, or request your vendor to supply their statement via this document.
- Import the Excel sheet:
  - Click on Import/Export again.
  - Select the option ‘Import Statement’.
  - Navigate to the saved Excel file and select it.
  - The system will load the entries from the sheet into the recon lines. If it is able to find the document using the external document number, it will load the statement amount into the existing line.  If not, it will create a new line with the statement amount.

## Reconcile transactions
Definition of fields on transactions

| Field Name | Source |
|------------|--------|
| Document date | When loaded from Vendor ledger – the document date on the vendor ledger entry<br>When loaded from statement – the document date on the import sheet, or the date manually captured by the user. |
| Document Type | Loaded from the vendor ledger entry OR from the statement import. |
| Document No. | From Vendor Ledger entry – non-editable. |
| External document no. | When loaded from vendor ledger – the external document on the ledger entry<br>When loaded from statement – the document number on the import sheet, or the document number |
| Due Date | Loaded from vendor ledger entry;<br>Editable if transaction is not in ledger |
| Ledger Amount | Total of original transaction from vendor ledger entry – not editable |
| Remaining amount | Unpaid portion of transaction from vendor ledger entry – not editable |
| Statement amount | Transaction amount reflected on supplier's statement – editable |
| Match status | **Unmatched** – default value<br><br>**Matched** – selected when statement amount and ledger amount agree. Option cannot be selected if the statement and ledger don't agree.<br><br>**Partial / on hold** – selected when entry is in ledger and on statement but remaining amount and statement amount do not agree.<br><br>**Carry forward** – selected when the entry is on the vendor statement but missing from ledger.<br><br>**Previously paid** – selected when entry is on the statement but remaining balance in ledger is zero<br><br>**Rejected** – manual selection, to indicate that payment will be withheld. |
| Amount to Match | Reflects the lower of Statement amount and Remaining amount on ledger; not editable. |
| Amount to Pay | Initially set to amount to match; can be overridden. |
| Comments | Manual entry of notes |

As entries are loaded from the system and the statement, the recon function will attempt to match them automatically, using the External document number from the system to match against the vendor's document number.

As entries are loaded from the system and the statement, the recon function will attempt to match them automatically, using the External document number from the system to match against the vendor’s document number.

If a match can be made on the document number, the transaction values from the system and the statement will be loaded on a single line alongside each other.  If the amounts from both sources match, the system will:
- Tick the ‘Matched’ column 
- Set the Matched status to ‘Matched’
- Set Amount to Match and Amount to Pay to the ledger amount.
 
![alt text](MatchingAmounts.png)

If the amounts don’t match, the lesser of Statement Amount and Ledger amount will be recorded into Amount to Match and Amount to Pay.

## Capture deductions
If deductions or Withholding tax are applicable, these are captured as follows:
- Select the ‘Payment’ menu and click on ‘Calculate Deductions’.
- If default deduction codes have been configured for the vendor, they will be automatically created for each invoice / credit note on the recon.  If set up with a percentage, this will be automatically captured.
- You can edit or add the deductions created per document. Select the line you want to update the deductions, and select Deductions from the subpage Matching menu.

![alt text](SelectDeductions.png)

## Handling Settlement Discounts
Business Central has the ability to manage settlement discounts when paying vendors. To enable this, the following conditions must be in place:
- Settlement discount must be configured on payment terms. (You can learn about this here: [Payment Terms in Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-payment-terms))
- The invoice(s) being settled must contain a date in the field 'Payment Discount Date', and a value in Remaining Discount.
- The Payment date for your reconciliation must be on or before the Payment Discount Date.

### Manually overriding settlement discounts

You can update the settlement date and value on the vendor ledger entries. This should be done BEFORE you 'suggest lines' on the reconciliation.
- Navigate to the vendor ledger entries page.
- Find the transaction you would like to modify.
- Click on 'Edit List' in the action bar.
- Update the Pmt Discount Date and Remaining Pmt. Disc. Possible as required.

![alt text](DiscountOnVLE.png)

When you run 'Suggest Lines', the transactions will be loaded. If settlement discount is applicable for an invoice, it will appear in the column 'Discount Available'.

![alt text](DiscountAvailable.png)

When you create the payment journal for the reconciliation, standard Business Central functions will deduct the settlement discount from the amount paid out of the bank account.

## Calculate the payment
After entries have been matched, and deductions calculated, you can calculate the payment entries for the recon.  Before doing so, check that a journal batch template and journal batch have been selected on the recon header.

![alt text](SelectJournal.png)

Click ‘Calculate Payment Amount’ on the Payment menu.  

Payment entries will be displayed in the Payment grid at the bottom of the screen. The default bank account is assigned from the batch that is set on the header. If deductions have been taken on any of the invoices, an entry per GL account will also be displayed in the payment grid:

 ![alt text](PaymentEntries.png)

If necessary, you can amend the payment allocation to use a different bank account, or split the payment between multiple bank accounts.

## Approve the reconciliation
After completing the payment calculations, the reconciliation needs to be approved for payment. From the payment menu, click on 'Request Approval'.

Depending on the approval method being used, this will either trigger the standard approval workflow process, or wait for a supervisor to approve.

## Approve and post the reconciliation
After the relevant users have approved the recon, it can be posted.  
Click on 'Post Reconciliation'.

 ![alt text](PostRecon.png)

There are two options for this:
- Generate and post the payment, which will settle the matched invoices on the vendor account, and process an entry against the bank account
- Archive the document without posting a payment.

From the popup, select the option you want.

![alt text](CreatePayment.png) 

- To close the reconciliation without posting the payment, click on ‘Archive’, then OK. This will change the status of the document to ‘Archived’, and it will no longer be editable.
- To generate a payment journal for the reconciliation, click on ‘Create Payment’. This will add the entries in the payment grid to the journal specified in the document header. The payment journal will be opened after the entries have been generated. 
- If you exit the batch without posting, the entries will remain there, and further recons will be added to the batch on posting.  
- If you post the journal, the invoices linked to the payment will be closed, and the creditor’s balance will be debited. The reconciliation status will be changed to ‘Archived’.

## Print or email documents
After processing your reconciliation, there are three documents that can be printed.
- Recon Statement -  provides a reconciliation between the balance owed according to the vendor’s ledger and the statement presented by the vendor.
- Remittance advice – provides details of invoices being settled.
- Payment authorisation – similar to the recon, providing details of differences between the supplier’s statement and the vendor ledger in a tabular format.

From the Reconciliation page, select the ‘Print documents’ menu, and select the document you wish to print.

## Review archived reconciliations
On the vendor reconciliation list page:
- Select the ‘Archived’ option in the filter panel

![alt text](ArchivedRecons.png)

Click on the recon number to open the reconciliation.

## Find a document

Search for 'Vendor Recon Document Search'.

![alt text](image.png)

Enter a document number or external document number and press Enter. The system will display a list of all recons on which the document occurs:

![alt text](image-1.png)

You can open the recon by clicking on the recon number.

[**⬆️ Back to Top**](#content) &nbsp;&nbsp;&nbsp;&nbsp; [**🏠 Home**](/trade_assistant)
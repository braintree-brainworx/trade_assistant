---
layout: NewLayout
title: Braintree Landed Cost 
description: Support and documentation for Braintree's Landed Cost extension to Microsoft Dynamics 365 Business Central
---

# Landed Cost

## [Adding landed costs to purchase orders](#create-landed-costs-on-purchase-orders)
## [Accruing landed costs](#accrue-costs-on-purchase-receipts)
## [Posting actual landed costs](#posting-landed-cost-invoices)

---

## Create landed costs on purchase orders
**Create a new order**
Create a new purchase and capture lines for the items to be purchased, as per normal Business Central processing.

If the item you selected is linked to a landed cost template, the code will be inserted on the order line:

  ![alt text](image-7.png)

You can amend the code, or insert a template code into lines which are not linked to landed costs templates.

**Generate Surcharges for Landed Cost:**
After entering all lines and assigning landed cost templates, click on 'Generate Surcharges':

  ![alt text](image-8.png)

For each purchase order line which has a landed cost template attached, surcharge lines will be created, using the item charges associated with the template:

  ![alt text](image-9.png)

The calculation type, calculation rate and preferred vendor will be defaulted from the template. You can amend these if required.

More charges can be added manually to the list if desired.

**Generate Surcharge Orders:**
For each surcharge, ensure that a vendor has been captured into the 'Service Provide' column.  Click on 'Generate Surcharge Orders'.

  ![alt text](image-10.png)

For each service provider used on the surcharge lines, a purchase order will be created for later use. The order number is inserted into the column 'Surcharge Purchase Order No.". You can view the orders by clicking on the order number:

  ![alt text](image-11.png)

  ![alt text](image-12.png)

## Accrue costs on purchase receipts
If you have attached landed cost surcharges to a purchase order, posting a receipt against the invoice results in additional entries for the relevant order lines.

In the General Ledger, landed cost provisions are be posted. The accounts affected are set up on the General Posting Setup.
- Debit  : Cost of Goods Sold
- Credit : Cost of Goods Sold (interim).

The associated purchase orders for the service providers will be updated to reflect the quantity received, and applied cost entries will be created.
  
  ![alt text](image-13.png)

  ![alt text](image-14.png)

## Posting landed cost invoices
Open the related landed cost order, either from the Purchase Orders list, or by clicking on the order number in the 'Surcharge Purchase Order No.' in the Surcharge Lines section of the primary purchase order:

  ![alt text](image-15.png)

For each line on the landed cost order, the associated Item Charge assignments are shown in the Item Charges list below:

  ![alt text](image-16.png)

The item charges assignment lines will reflect the receipt details from the primary purchase order. 

Update the order with the supplier's invoice number and amend dates as required. Post the invoice.

A posted invoice will be created according to standard BC processes. In addition, GL entries will be processed to reverse the accrual raised from the primary order receipt, and actual costs will be posted in the normal way.

[**⬆️ Back to Top**](#landed-cost) &nbsp;&nbsp;&nbsp;&nbsp; [**🏠 Home**](/trade_assistant)
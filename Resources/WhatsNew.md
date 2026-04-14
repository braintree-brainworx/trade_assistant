## Release notes

**Release 27.4.20260409.1 (27.4.2)**
<details style="font-size: 0.85em;">
<summary>Posted Sales Invoice List</summary>
<ul>
<li>Add Last Date Emailed to page</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Dispute State</summary>
<ul>
<li>On Collections Link page, Reason Code is now linked to new table Dispute State</li>
<li>When a reason is entered, the Dispute State on Customer Ledger Entry and posted invoice is updated.</li>
</ul></details>

**Release 27.4.20260409.1 (27.2.7)**
<details style="font-size: 0.85em;">
<summary>Landed Cost</summary>
<ul>
<li>Accrue item charges into GL provision accounts when primary products are received, and reverse accrual when item charges are invoiced</li>
</ul></details>

**Release 27.2.20260327.1 (27.2.7)**
<details style="font-size: 0.85em;">
<summary>DCM: Cosmetic changes (click for details)</summary>
<ul>
<li>Collections Dashboard - switch FactBoxes around</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: New report - Collection Note (click for details)</summary>
<ul>
<li>From a collection note, an option is added to generate a RDLC report of the collection note.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>User Setup: New option to generate User Setup records from registered users(click for details)</summary>
<ul>
<li>When accessing the user setup list from Trade Assistant Setup, an action, 'Create Users', has been added. This will create users in User Setup if they do not exist and create a payment journal batch for each user. </li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>VRS: Deductions (click for details)</summary>
<ul>
<li>Deduction code lookup to Return Reasons table is filtered for entries with a GL account number. Return reasons not linked to GL are not available for selection.</li>
</ul></details>

**Release 27.2.20260219.1 (27.2.4)**
<details style="font-size: 0.85em;">
<summary>VRS: payment reference  (click for details)</summary>
<ul>
<li>When generating the payment journal from a Vendor Recon, the payment reference will be populated with the creditor's account number.</li>
</ul></details>

**Release 27.2.20260213.1 (27.2.4)**
<details style="font-size: 0.85em;">
<summary>DCM: Bug: customer FactBox on collection note (click for details)</summary>
<ul>
<li>The DCM collection note shows wrong customer: data link added to select customer associated with note.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Collection note creation (click for details)</summary>
<ul>
<li>when adding a document to a collection note, reason codes and notes are copied from last collection note</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Collection Dashboard (click for details)</summary>
<ul>
<li>Added menu options to display reminders and finance charge memos</li>
</ul></details>

**Release 27.2.20260211.1 (27.2.3)**
<details style="font-size: 0.85em;">
<summary>DCM: Handling Zero-balance accounts (click for details)</summary>
<ul>
<li>The DCM dashboard now includes an option to show or hide customers with a zero balance.
The DCM dashboard now includes an action to remove summary notes from accounts with zero balances.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Link to Reminders (click for details)</summary>
<ul>
<li>Issued Reminders are accessible from the Collection Dashboard and from the subpage for the selected customer.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>VRS: Transactions on Hold (click for details)</summary>
<ul>
<li>Vendor Ledger entries which have been place on hold can be reconciled, but not settled via a vendor recon</li>
</ul></details>

**Release 27.0.20260115.2 (27.2.1)**
<details style="font-size: 0.85em;">
<summary>VRS: Bug using attachments with Service Documents (click for details)</summary>
<ul>
<li>Attempting to attach a document to a service document resulted in an error. Issue has been resolved.</li>
</ul></details>

**Release 27.0.20260107.3 (27.2.1)**
<details style="font-size: 0.85em;">
<summary>Trade assistant role centre (click for details)</summary>
<ul>
<li>New role centre created to access all trade assistant documents. Set user profile to 'Braintree Trade Assistant'.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Collection Note Search (click for details)</summary>
<ul>
<li>Search for a document number and view the collection notes on which it appears. <a href="{{ '/DCM/RunDebtors#find-a-document' | relative_url }}">Learn more</a></li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Collection Note Document (click for details)</summary>
<ul>
<li>After creating and updating a collection note, you can now generate a PDF or hard copy of the collection note.</li></ul></details>

<details style="font-size: 0.85em;">
<summary>DCM: Debtors Admin Customer list (click for details)</summary>
<ul>
<li>New report listing customers per debtors administrator</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>VRS: Disable actions on archived document (click for details)</summary>
<ul>
<li>Actions relating to calculations and payment creation are disabled on the Vendor Recon card if the status is Archived</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>VRS: Supplier Performance Report (click for details)</summary>
<ul>
<li>New report showing supplier reliability on purchase orders</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>VRS: Unmatched GRV's (click for details)</summary>
<ul>
<li>New report showing purchase orders not delivered, or delivered and not invoiced.</li>
</ul></details>

<details style="font-size: 0.85em;">
<summary>FEC: Bug fix: message  (click for details)</summary>
<ul>
<li>Debugging message in OnSetApplyToAmountOnBeforeVendEntryEdit removed.</li>
</ul></details>

**Release 26.0.20251212.2 (27.1.1)**
<details style="font-size: 0.85em;">
<summary>VRS: Search for a vendor document number (click for details)</summary>
<ul>
<li>From the vendor ledger page, or vendor recon list, select 'Find Vendor Reconciliation, enter a document number or external document number. All recons on which the document appears will be listed. Click on the recon number to open the recon.  <a href="{{ '/VRS/RunVendorRecon#find-a-document' | relative_url }}">Learn more</a>
</li>
</ul></details>

**Release 26.0.20251212.2 (27.1)**
<details style="font-size: 0.85em;">
<summary>VRS: Report layout - Payment authorisation (click for details)</summary>
<ul>
<li>Font in detail changed to Calibri 7pt.</li>
<li>Document columns changed to allow wrap.</li>
</ul></details>

**Release 26.0.20251126.1 (26.6)**
<details style="font-size: 0.85em;">
<summary>VRS: When suggesting lines, system requires response to prompt for discount (click for details)</summary>
<ul>
<li>Message is suppressed if discount value on vendor ledger entry is the same as discount available on recon line.</li>
</ul></details>

**Release 26.0.20251124.3 (26.5)**
<details style="font-size: 0.85em;">
<summary>1. VRS: Error message: Amount to pay does not equal matched amount" when clicking on 'Request Approval' (click for details)</summary>
<ul>
<li>Modified filter before calculating totals</li>
</ul></details>

<!-- next issue -->
<details style="font-size: 0.85em;">
<summary>2. VRS: The Remittance Advice also does not show the actual net payment correctly when discount is taken (click for details)</summary>
<ul>
<li>Report layout adjusted to include new columns for Discount Claimed and Other deductions.</li>
<li>Font reduced to 7pt to accommodate new columns</li>
<li>Calculation of nett payment adjusted to deduct discount and Other Deductions</li>
</ul>
</details>

<!-- next issue -->
<details style="font-size: 0.85em;">
<summary>3. VRS: On 'Request Approval', when matched amount and payment amount don't match, clicking No on the confirmation dialog has no effect (click for details)</summary>
<ul>
<li>Click on No now results in operation being cancelled.</li>
</ul>
</details>

**Release 26.0.20251121.1 (26.4)**

<details style="font-size: 0.85em;">
<summary>VRS: Allow selected users to override payment discounts from Vendor Recon page (click for details)</summary>
<ul>
<li>Trade assistant user setup: new field "Allow Discount Modify"</li>
<li>If turned on, user can edit Discount Available on recon lines</li>
<li>When discount is edited, user will be prompted to confirm.</li>
<li>Discount amount will be transferred to vendor ledger entry</li>
<li>Pmt Discount date on vendor ledger entry will be set to Recon payment date + 1 day</li>
</ul></details>

**Release 26.0.20251119.1 (26.3)**
<details style="font-size: 0.85em;"> 
<summary>VRS: Manage settlement discount</summary>
<ul>
<li>Requirement: Handle settlement discounts on invoices being settled.</li>
<li>Changes:
  <ul>
  <li>field added to Vendor Recon subpage to display discount available from vendor ledger</li>
  <li>when Suggest Lines is run, IF payment date is less than Discount date on vendor ledger, AND discount is avalalbe, the remaining discount will be populated.</li>
  <li>discount is provided for info only - will show on reports</li>
  <li>discount will be applied to vendor payment when the payment journal is posted, using standard BC settlement discount function</li>
  </ul>
</li>
</ul></details>
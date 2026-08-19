# Configure Debtors Collections

- [Installing from AppSource](#installing-from-appsource)
- [How to request a license registration key](#how-to-request-a-license-registration-key)
- [Number Series](#number-series)
- [Ageing Setups](#ageing-setups)
- [Dispute Reasons](#dispute-reasons)
- [Updating Customers](#updating-customers)

## Installing from AppSource
Open your Microsoft Dynamics Business Central tenant.
Search for Extension Management.
From the extension management page, select 'AppSource Gallery'. This may take a minute or two to open.
Search for Braintree.
Select 'Braintree Trade Assistant'.
Click on Install App:

![alt text](InstallApp.png)

After the app has installed, the setup page will open. The first thing you need to do is request a licencs key.

## How to request a license registration key
From the Trade Assistant Setup page.
From the menu bar, select 'Register App':

![alt text](RegisterApp.png)

From the list of apps, select 'BCP-TRADEASSIST-DCM', then select 'Request Subscription / Trial license' from the menu bar:

![alt text](RequestSubscription.png)

An email will be sent to the Braintree service desk. Once the request has been registered, a support consultant will send you a registration key. On the subscription request page, click on 'Update License Key':

![alt text](UpdateLicence.png)

Enter the key provided in the input box, and click OK.

![alt text](EnterLicenceKey.png)

## Number Series

On installation, the system will create a new number series and insert it in the setup table. You can edit this if required.

## Ageing Setups
Ageing Setup: used to define default settings and column headings on the collection dashboard.
Select Ageing Setup from the menu.
Add at least one setup definition:
- Code: enter a code to identify the setup.
- Ageing Type: select Accounting Period, Custom, or Calendar month
- Ageing By: select Document Date, Posting Date, or Document Date
- If using Custom ageing, enter a date formula to define the length of the periods eg 30D
- Enter appropriate column headings for each ageing bucket. For example, enter '30D' or '30 Days'. This will be displayed as the column heading on the Debtors Collection Dashboard.

 ![alt text](AgeingSetup.png)

## Dispute Reasons
From the Trade Assistant Setup, click on Dispute Status in the menu.
The Dispute Statuses page will be displayed.
Add new codes as required.

## Updating Customers
For each customer, set up the collections administrator for the account.
Open the customer card.
Go to the Invoicing tab.
In the section labelled ‘Trade Assistant’. 
In the field ‘Collections Administrator’, select a user name.

![alt text](CustomerCard.png)

[**⬆️ Back to Top**](#content) &nbsp;&nbsp;&nbsp;&nbsp; [**🏠 Home**](/trade_assistant)
<h3>10/27 Release</h3>

Now using fields from upstream systems to automatically delegate POs to the correct Manager and Delegated Time Verifier- will reduce onboarding time:
Manager email and Delegated Time Verifier (if applicable) are now required fields in the upstream systems we pull our PO data from, so we are utilizing this to automatically delegate POs to the correct managers and assign the  

Now keeping track of "real-time" funds on the PO to govern time sheet verification:
Once a Purchase Order is pulled into our app from BDW (our SOR), we will take a snapshot of the number of hours and expenses available on the Purchase order, creating an "internal value" for our application. From that point forward, when a time sheet is fully verified, the hours will be subtracted from this value, and likewise for expenses. Rejected time sheets will not affect this internal value. A time sheet cannot be verified by the manager or supplier if it will cause the internal value to become negative. 

Time Sheets that were locked due to having been invoiced can now send to ILC correctly :
Once a time sheet is marked as having been invoiced, that time sheet is locked in the Blockchain application. Changes to the time sheet must be made as "Post-Processing Edits" where the changes are made as positive or negative "delta" values. Because of the complexity of working with these delta values, changes to the ILC codes made after invoicing would have to be submitted in ILC directly, but now, we will tabulate the new totals and send the updated overall values to ILC. 

Accessibility enhancements:
We are trying to make sure our app stays compliant with accessibility standards so that everyone can use our application regardless of any impairments they may have 

Defect with not being able to clear Notifications resolved:
There was a defect where the notifications under the bell icon could not be cleared. We have resolved this and you should be able to clear individual notifications or clear all notifications that are visible on the page

-- 2020 Highlights --

We added a timesheets page allowing contractors to see a table of ALL of their timesheets, including saved (not submitted) timesheets and timesheets on multiple POs

In response to manager feedback, we created a new landing page which clearly presents all of the items awaiting action.

We introduced a variety of reports that allow Managers, Delegated Time Verifiers, Financial Analysts, IBM Contractor Administrators, and Suppliers to keep track of and have better insight into their contractor and Purchase Orders.

Weekly emails to remind Managers and DTVs about time sheets that need to be verified

Made it so that if there is a renewal PO that flows to the app and is linked in CSA to a PO already in the Blockchain Application with an "All Approved" contractor record, the contractor record on the new PO will automatically be created.

New tab added to Purchase Orders page: "Pending Contractor Assignment"- this tab will show the new and renewal POs loaded to the application that do not yet have a contractor associated to them.

Made it so that when a new timesheet is loaded, we will only copy over the valid timesheet rows from the previous week's timesheet.

Upgraded to IBM Blockchain Platform (IBP) v2


**9/1**

When switching tabs, instead of reloading the full page and presenting a loading symbol in the middle of the page, we'll present the loading symbol in just the tab that is being loaded.

We received feedback that on certain monitors, the font on the time sheet page was difficult to see and lacked contrast. In response to this feedback, we've increased the boldness of the font so it is easier to read.

In response to manager feedback, we created a new landing page which clearly presents all of the items awaiting action. There are four main components:

The time sheets which are pending your verification
The contractor records which are pending some action on your side to be fully set up
New POs that have come in but do not have a contractor record set up against them
POs which are expiring within the next 8 weeks and thus could necessitate a renewal PO if the contractor is to continue working.
Once any of these four is zero (meaning you have no pending action), the text will turn from red to green for that component.

We added a new Expiring tab on the Purchase order page which shows all POs where the PO will end within 8 weeks of the current date. This is a heads up to you about the POs for which you need to work on a renewal due to the upcoming end date.

The Inactive PO and Contractors tabs will now be tied. When you move a PO to inactive, any contractor records associated with the PO will also move to the inactive tab, and visa versa

Contractor start and end date now shows up in the csv export of the PO table

Reports!

We introduced a variety of reports that allow Managers, Delegated Time Verifiers, Financial Analysts, IBM Contractor Administrators, and Suppliers to keep track of and have better insight into their contractor and Purchase Orders. The Reports can be accessed through the menu in the top right corner of your screen.

Contractors Not Claiming

This report shows all contractors that

Are within the start and end dates on their PO
Are in "All Approved" status
Have not been moved to your inactive tab
Have not yet submitted a timesheet in the blockchain app
Remaining Funds

This report shows a list of all POs that have 20% or less of funds remaining on any of the line items, for POs that are not on your inactive or cancelled tabs.

Expiring Contractors

This report shows a list of contractors that are 8-weeks or less in advance of the contractor end date, that are not on your inactive tab

ILC Hours

Via this report, Managers and DTVs can now see in bulk the timesheet details by serial num and line item the ILC codes logged by ILC contractors including account id, work item id, activity code, and bill code

Liability/Invoice Enhancement

We have added Additional filtering capabilities for the existing Liability and Invoice Reports


7-7--

New Timesheets Page

We added a timesheets page allowing contractors to see a table of ALL of their timesheets, including saved (not submitted) timesheets and timesheets on multiple POs. This gives the contractor the ability to see the status of all of their submitted timesheets in a single view. This table can be downloaded and searched, it also shows the email of the manager, DTV and SAM who need to verify the timesheets.

PO Cancellation

This new function allows our application to process in a Purchase Order Cancellation from the upstream applications (Buy@IBM/Ariba). Once the PO has been cancelled, the Purchase Order and Contractor Record (if one was created prior to the cancellation) will be moved to the Cancelled tabs (Managers/CCA/FA/SAM). The Manager and the Supplier will receive an email notifying them that the PO was cancelled. We have created a function to allow timesheets on the cancelled PO to be migrated off of the Cancelled PO onto a renewal PO. This function is brand new so we highly recommend you read the training documentation in the PDF

For managers who are part of GBS or GTS, if the contractor admin teams move a PO or a contractor to their inactive tab, the PO or contractor record will also move this record for the assigned manager as well. This function helps keep the offboarding process more in sync and should help limit the automated reminder emails informing managers that the PO is running out of funds or the contractor records are expiring soon.

A new email will come out weekly to notify managers and DTVs when the have timesheets on their escalated tab. Since timesheet verification is an important weekly activity, we will be sending out weekly reminder emails for all timesheets which are escalated which means they have not been verified before the escalated deadline.


--4/28--
Made it so that if there is a renewal PO that flows to the app and is linked in CSA to a PO already in the Blockchain Application with an "All Approved" contractor record, the contractor record on the new PO will automatically be created.


--3/11--
Search function on Timesheets page enhanced to allow users to search by more fields Enabled ability to search by billing start date and billing end date on the Invoice Reconciliations page

Added the PO Start date and PO End date added to Purchase Orders bulk page table Enabled ability to SORT on the Purchase Orders bulk page (can sort by clicking on the column headers)

Removed "Manage ILC Accounts" option from the menu drop-down. This page is no longer used as contractors have ability to SEARCH and SELECT their valid ILC accounts

Delegated Time Verifiers will now have ability to migrate pending timesheets to the new/ renewal PO (ability previously held only by Managers)

Managers will now have a way to view, change, and delete scheduled DTV assignments on the new "DTV Schedule" page. This is for temporary DTV assignments, not permanent assignments.

New tab added to Purchase Orders page: "Pending Contractor Assignment"- this tab will show the new and renewal POs loaded to the application that do not yet have a contractor associated to them.

Contractor start and end date now pre-populated based on the information on the Purchase Order data in Ariba.

Timesheet enhancements for Contractors: Made it so that when a new timesheet is loaded, we will only copy over the valid timesheet rows from the previous weeks timesheet. For example If the ILC account claimed against this week expires at the end of this week, it will not be pre-populated to next weeks timesheet.

Timesheet rows will be marked as invalid if MANUALLY entered by user and NOT selected/validated. This will help with the "Invalid ILC Account" error before submitting timesheets. Only selected search entries will be valid entries able to be claimed against

More obvious Search button for searching ILC accounts

Added new function to allow users to clear out their ILC accounts for an entire line at a time

POs/ Contractors will now automatically move to "Inactive" tab for CCA and Mgr automatically after the 4-week grace period has passed

Enabled ability for admins to search by role or by email address on the Users page

We are continually trying to make your experienced more streamlined and enjoyable. Many of these enhancements came as a direct result from your feedback!

# Kasper Support Troubleshooting Reference

This guide covers common issues, what probably caused them, and the steps to fix them. Since everything in Kasper syncs with Open Dental, most of these issues are usually just setup mistakes or bad data inside Open Dental, not an issue with Kasper itself.

## Scheduling and Opportunity Finder

### 01. Opportunity Finder shows no matches for an open slot
* Check Open Dental and make sure the treatment plans are actually set to "Treatment Planned". If they are marked as completed, rejected, or blank, they won't show up.
* Make sure the treatment type you picked in Opportunity Finder actually matches the procedure codes in the patient's plan. If they don't match, you get zero results.
* Check if the patient's preferred provider or operatory settings in Open Dental are blocking the match. Try turning off some filters to see if that helps.
* Make sure the Open Dental sync is actually running under Settings -> Integrations. If the sync is stuck, the treatment plan data won't be updated.
* NOTE: If the plans look good and the sync is working but nothing shows up, get the patient's name, the code, a screenshot, and escalate it.

### 02. Online booking shows no slots but the schedule looks open
* Go to Settings -> Online Scheduling and make sure that specific appointment type is actually turned on for online booking.
* Check for schedule blockouts in Open Dental for those dates. Blockouts will hide slots on the online widget.
* Make sure the provider or operatory for that appointment type is set to available in your Online Scheduling settings.
* Check the sync status. If Kasper is lagging behind Open Dental, it might be hiding open slots by mistake.

## Phone and Call Intelligence

### 03. Caller ID pop up not showing up when someone calls
* Make sure the VoIP phone or softphone is online and the user has their extension assigned under Settings -> Team Management.
* Check the patient's phone number in Open Dental. It has to match the incoming caller ID exactly. If the formatting is weird, it won't match.
* If it's a brand new patient who isn't in Open Dental yet, the pop up won't show up. That's normal. You have to make the account after the call.
* Make sure the Kasper desktop app or browser tab is actually open and active on that computer, or the pop up won't trigger.
* NOTE: If this used to work and suddenly stopped, ask if IT changed any firewall or VoIP settings recently. That's usually why.

### 04. Call Intelligence isn't transcribing or giving summaries
* Make sure the Call AI add-on is actually enabled under Settings -> Billing since it's a separate paid feature.
* Check if call recording is turned on for those specific extensions. No recording means no transcript.
* Wait a few minutes. The system takes a bit to process the text after the call ends. 
* Check the call length. Super short calls (under 10 seconds) won't get a summary.
* CRITICAL: If recording is definitely on and it's missing summaries for a bunch of long calls, escalate it with the call log IDs.

## Digital Forms

### 05. Patient sent a form but it's missing in Open Dental
* Look up the patient in Kasper and make sure the status says "Submitted". If it says "Sent" or "Pending", they probably missed a required question and didn't finish it.
* Check the sync status in Settings -> Integrations. A broken sync will hold the forms in Kasper.
* Make sure the form got linked to the right patient. If they used a generic link, it might have made a duplicate account or got stuck as unmatched.
* Try hitting refresh inside Open Dental. Sometimes the data is there but the screen just hasn't updated.
* TIP: While you figure it out, the staff can just copy the info from Kasper and type it into Open Dental manually so they can check the patient in.

### 06. Patient says they never got the link for the form
* Check the patient's file in Open Dental to make sure their phone number and email are correct and not blank.
* Open the patient's record in Kasper and check the send log to see if the message says "Delivered" or "Failed".
* Have the patient check their text spam folder or email spam folder.
* Just click resend manually from Kasper. If they are already standing at the front desk, just use the iPad fallback so they can fill it out right there.

## Insurance Verification

### 07. Insurance verification gives an error or nothing happens
* Open the insurance info in Open Dental and make sure carrier name, subscriber ID, group number, and DOB are all filled out. If any of those are blank, the check fails.
* See if the carrier is actually supported for auto-checks. Some small insurance companies don't work with the system and you have to call them manually.
* Make sure the patient's plan isn't expired or in a waiting period, because the insurance company might just say they are inactive.
* If they have secondary insurance, make sure both are put into Open Dental correctly.
* NOTE: If the carrier is supported and everything is filled out but it still fails, get the carrier name and subscriber ID (hide any private info) and escalate it.

## Payments and KasperPay

### 08. Payment went through but didn't post to Open Dental ledger
* Check the sync status under Settings -> Integrations. A bad connection will stop KasperPay from posting to the ledger.
* Make sure the staff member who ran the card actually has permission to write to the ledger inside Open Dental. If they don't, it blocks it silently.
* Look at the KasperPay transaction log. If it says "Pending Allocation", it means the payment cleared but couldn't map to a procedure because codes are missing or messed up in Open Dental.
* Refresh Open Dental to see if the ledger updates.
* CRITICAL: Do not swipe the card again until you check the KasperPay log. You don't want to double-charge the patient.

### 09. Automatic payment failed on a plan and the patient didn't get a text
* Check the end-of-day payment report in Kasper to verify the failure actually happened.
* Check the mobile number in Open Dental. If it's wrong, the automatic text alert obviously went to the wrong number.
* See if the card on file is expired by checking the payment plan details in Kasper.
* Just send them a manual text-to-pay link from Kasper so they can update their card and pay the balance.

## Open Dental Sync

### 10. Kasper data is old or not updating from Open Dental
* Go to Settings -> Integrations and check the last sync time. If it's more than a few minutes old, the connection probably dropped.
* Make sure the main Open Dental server computer at the office is turned on and connected to the network.
* Ask if they just updated their Open Dental software version. Big updates can break the sync and require support to fix it.
* If they use a VPN for their office network, make sure it's actually running on the server.
* CRITICAL: Escalate to Tier 2 immediately if the sync has been totally dead for over 15 minutes during regular business hours.

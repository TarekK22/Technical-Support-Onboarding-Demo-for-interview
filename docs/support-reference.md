# Technical Support — Troubleshooting Reference

Common issues, likely causes, and step-by-step checks. All Kasper features sync with Open Dental — most tickets trace to either a configuration gap or a data issue in Open Dental rather than Kasper itself.

---

## 📅 Scheduling & Opportunity Finder

### 01. Opportunity Finder shows no matches for an open slot
1. **Confirm treatment plans are entered in Open Dental** with status **Treatment Planned** — not *Completed*, *Rejected*, or left blank.
2. **Check that the treatment type selected** in Opportunity Finder matches the procedure codes on the patient's plan. A mismatch returns no results.
3. **Confirm the patient's preferred provider and operatory** in Open Dental aren't restricting the match. Widen filters if needed.
4. **Verify that the Open Dental sync is active** under `Settings → Integrations`. If the last sync timestamp is stale, treatment plan data may not be current.

> ⚠ **Note:** If treatment plans are correctly entered and syncing but still not appearing, collect the patient name, procedure code, and a screenshot and escalate.

### 02. Online booking shows no available slots even when the schedule has openings
1. **Check `Settings → Online Scheduling`** and confirm the appointment type the patient is trying to book is enabled for online booking.
2. **Look for schedule blockouts** in Open Dental covering that date range — blockouts suppress available slots in the widget.
3. **Confirm the provider or operatory** associated with that appointment type is marked as available in the Online Scheduling settings.
4. **Verify the Open Dental sync is live.** If the schedule in Kasper doesn't reflect recent Open Dental changes, a sync lag may be hiding available slots.

---

## 📞 Phone & Call Intelligence

### 03. Caller ID screen pop not appearing when a patient calls
1. **Confirm the VoIP phone or softphone is active** and the user's extension is assigned in `Settings → Team Management`.
2. **Check that the patient's phone number in Open Dental matches** the inbound caller ID exactly — including country code format. A format mismatch prevents the lookup from matching.
3. **If the caller is a new patient** with no Open Dental record, no pop will appear — this is expected behavior. A new patient record should be created during or after the call.
4. **Confirm the Kasper desktop app or browser tab is open** and in focus on the receiving workstation. The pop requires an active Kasper session.

> ⚠ **Note:** If pops worked previously and stopped, check whether a VoIP configuration change or firewall update occurred recently — these are the most common causes of a sudden regression.

### 04. Call Intelligence not transcribing or summarizing calls
1. **Confirm the Call AI add-on is active** on this account under `Settings → Billing`. Call Intelligence is a separately priced module — it won't transcribe if not enabled.
2. **Check that call recording is turned on** for the relevant extensions. Transcription requires a recorded call — no recording means no transcript.
3. **Transcription processes after the call ends** — there is a short delay (typically under a few minutes). If the summary is missing an hour or more after the call, proceed to the next step.
4. **Very short calls (under 10 seconds)** may not generate a summary. Check the call duration in the call log.

> 🚨 **CRITICAL:** If call recording is confirmed on and summaries are consistently missing across multiple calls, escalate with the affected call log IDs.

---

## 📝 Digital Forms

### 05. Patient submitted a form but it's not showing in Open Dental
1. **In Kasper, go to the patient's record** and confirm the form shows status **Submitted** — not *Sent* or *Pending*. If still Pending, the patient may not have completed all required fields.
2. **Check the Open Dental sync status** in `Settings → Integrations`. A sync delay or disconnection will hold form data in Kasper without pushing it across.
3. **Confirm the form is mapped to the correct patient record.** If a form was submitted via a generic link without pre-population, it may have created a duplicate or unmatched record.
4. **Refresh Open Dental on the workstation** — data may have synced but not yet appeared in the current view.

> ✅ **Tip:** As a temporary fix while investigating, staff can manually enter the patient's information from the Kasper submission view into Open Dental to unblock the appointment.

### 06. Patient says they never received their form link
1. **Check the patient's contact details in Open Dental** — confirm the mobile number and email are correct and not blank.
2. **In Kasper, open the patient's record** and check the form send log. Confirm a send was attempted and note whether it shows *Delivered* or *Failed*.
3. **Ask the patient to check their SMS spam folder** or email junk folder — automated messages are sometimes filtered.
4. **Resend the form link manually from Kasper.** If the patient is in the office, use the iPad fallback to complete forms chairside.

---

## 🏥 Insurance Verification

### 07. Insurance verification returning an error or no results
1. **Open the patient's insurance record in Open Dental** and confirm all required fields are filled: **carrier name, subscriber ID, group number, and date of birth**. Missing any one of these will cause the eligibility check to fail.
2. **Check whether the carrier is supported** for automated verification. Some smaller carriers require a manual call — Kasper will indicate this if the carrier isn't in the network.
3. **Confirm the patient's plan isn't expired** or in a waiting period — the insurer may return a valid response that reads as inactive coverage.
4. **If the patient has secondary insurance**, make sure both plans are entered in Open Dental. Kasper verifies both when available.

> ⚠ **Note:** If the carrier is supported and fields are complete but verification still fails consistently, escalate with the carrier name and patient subscriber ID (redacted for privacy).

---

## 💳 Payments & KasperPay

### 08. Payment processed but not posting to the Open Dental ledger
1. **Check the Open Dental sync status** in `Settings → Integrations`. A broken sync connection will hold KasperPay transactions without posting them.
2. **Confirm the user who processed the payment has ledger-write permissions** in Open Dental. Permissions errors silently block posting without showing an error in Kasper.
3. **Open the payment in KasperPay's transaction log** and check whether it shows **Posted** or **Pending Allocation**. Pending Allocation means the payment arrived but couldn't be mapped to a procedure — this usually happens when procedure codes are missing or mismatched in Open Dental.
4. **Refresh Open Dental on the workstation** — the ledger may have updated but the local view hasn't refreshed yet.

> 🚨 **CRITICAL:** Do not process a second payment before confirming the first didn't post — this risks double-charging the patient. Verify the transaction log in KasperPay first.

### 09. Auto-payment on a payment plan failed and patient wasn't notified
1. **Check the end-of-day payment transactions report in Kasper** — failed auto-payments should appear here. If the report wasn't reviewed, the failure may have gone unnoticed.
2. **Confirm the patient's mobile number in Open Dental is correct.** Kasper sends an automatic text-to-pay follow-up on failed payments — a wrong number means the message never reached them.
3. **Check whether the patient's card on file has expired.** Open the payment plan in Kasper and review the card expiry date.
4. **Manually send the patient a text-to-pay link** from their Kasper account record so they can update their payment method and settle the balance immediately.

> ✅ **Tip:** Recommend the practice review their end-of-day payment report daily — this is the fastest way to catch failed charges before they compound.

---

## 🔄 Open Dental Sync

### 10. Kasper data appears out of date or not reflecting recent Open Dental changes
1. **Go to `Settings → Integrations`** and check the last successful sync timestamp. If it's more than a few minutes old during business hours, the connection may have dropped.
2. **Confirm the Open Dental server is running** and reachable on the practice's network. If the server was restarted or updated, the Kasper connection may need to be re-established.
3. **Check whether the practice recently updated their Open Dental version.** Major updates occasionally require a Kasper re-integration — contact support to confirm compatibility.
4. **If the practice uses a VPN**, confirm it's active on the server hosting Open Dental. A dropped VPN severs the Kasper connection without an obvious error.

> 🚨 **ESCALATION RULE:** Escalate to Tier 2 if the sync has been broken for more than 15 minutes during business hours.

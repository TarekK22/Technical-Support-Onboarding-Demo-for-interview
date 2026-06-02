ONBOARDING GUIDE

*Written as a Kasper onboarding specialist welcoming a new dental practice to the platform.*

---

# Welcome to Kasper
### New Practice Onboarding Guide

---

Welcome aboard. This guide covers everything you need to get your practice running on Kasper — from connecting Open Dental to making your first phone call through the system. We'll move through setup in the order that matters: foundation first, then communication, then supervision and revenue tools.

Before we start: Kasper syncs with Open Dental in real time. Every action you take in Kasper writes back to Open Dental automatically. You will not need to enter anything twice.

---

## Phase 1 — Foundation Setup (Day 1–2)

### 1.1 Connect Kasper to Open Dental

Kasper reads directly from your Open Dental database. Your onboarding specialist will walk through this with you, but here's what happens:

1. Your IT contact or office manager provides database access credentials
2. Kasper connects to your Open Dental instance (server-hosted or cloud)
3. Your patient records, appointment schedule, insurance data, and ledger are now live in Kasper

**Verify the sync is working:** Open Kasper and confirm you can see today's appointment schedule pulling from Open Dental. If any appointments are missing, check that the Open Dental appointment module is showing the correct date and provider filters.

**Common issue:** If your practice uses a VPN or has a firewall, you may need to whitelist Kasper's IP ranges. Contact support at support@meetkasper.com and your IT team will receive exact configuration instructions.

### 1.2 Set Up Your Team

Add every staff member who will use Kasper:

- Go to **Settings → Team Management → Add User**
- Assign roles: Front Desk, Office Manager, Provider, Admin
- Each role controls what the user can see and do (e.g., providers see clinical context; front desk sees scheduling and billing)

There is no per-user fee. Add everyone who needs access.

**Tip for office managers:** Set yourself up with Admin access. This gives you visibility into call intelligence reports, governance alerts, and the revenue leakage dashboard that other roles don't see by default.

### 1.3 Configure Your Phone System (VoIP)

Kasper replaces your existing phone system. This is often the step that feels biggest — it's also the one with the most immediate daily impact once it's done.

**What you need:**
- Your current phone number(s) — Kasper ports them over, patients notice nothing
- Physical phones or headsets for each workstation (Kasper supports most SIP-compatible hardware)
- Stable internet connection at each desk (minimum 5 Mbps per concurrent line)

**What Kasper sets up for you:**
- IVR call tree (your "press 1 for scheduling, press 2 for billing" menu)
- Call routing rules (which calls go to which staff)
- Voicemail boxes per extension
- Mobile app access for the office manager

Once phones are live: when a patient calls, a screen popup appears at the receiving desk showing their Open Dental chart — next appointment, last visit, balance, hygiene due date, and any unscheduled treatment. Your staff has full context before saying hello.

**Tip:** Keep your old phone service active for 48 hours during the port. Number porting takes 1–3 business days and calls may briefly route to either system during transition.

---

## Phase 2 — Patient Communication Setup (Day 2–3)

### 2.1 Set Up Automated Appointment Reminders

Go to **Settings → Reminders → Appointment Reminders** and configure:

- **7-day reminder:** SMS + email. Include the appointment date, time, provider name, and a link to confirm.
- **3-day reminder:** SMS. Short. Date, time, confirm/cancel link.
- **1-day reminder:** SMS. Same format.
- **1-hour reminder:** Optional. Recommended for new patients.

**Confirmation tracking:** Kasper shows you in real time which patients have confirmed and which haven't. Unconfirmed patients 24 hours out appear as a flag on your dashboard so a team member can call.

**Tip:** Keep reminder language friendly and direct. "Hi [Name], reminder: you have an appointment with Dr. [Name] on [Day] at [Time]. Reply YES to confirm or call us at [number]."

### 2.2 Set Up Digital Forms

Go to **Settings → Forms** to configure your paperless intake workflow.

Forms Kasper supports out of the box:
- New patient intake (health history, demographics, emergency contact)
- Medical history update (for returning patients annually)
- HIPAA consent
- Financial policy acknowledgment
- Treatment consent forms
- Post-op instructions (triggered automatically after specific procedure types)

**Sending forms:**
- New patient scheduled → Kasper automatically sends intake forms via text and email 48 hours before the appointment
- Returning patient → annual health history update triggers 7 days before their appointment

**In-office fallback:** If a patient arrives without completing their forms, the front desk can send a link from the check-in screen. The patient fills it out on their phone while waiting. The submission appears in their Open Dental chart within seconds.

### 2.3 Enable Online Scheduling

Go to **Settings → Online Scheduling** to activate the booking widget.

- Add the widget link or embed code to your practice website
- Set which appointment types are available online (new patient exams, hygiene, consultations)
- Set buffer times between appointments and blocked hours
- Enable or disable same-day booking based on your preference

When a patient books online, the appointment appears directly in Open Dental. No call needed, no manual entry, no risk of double-booking.

**Tip:** Limit online booking to hygiene and new patient exams initially. Emergency visits and complex restorative work should still come through the phone so staff can triage properly.

---

## Phase 3 — Insurance Verification (Day 3)

### 3.1 Activate Automated Eligibility Checks

Go to **Settings → Insurance → Automated Verification** and turn it on. Once active, Kasper runs eligibility checks for every patient with an appointment in the next 48 hours — overnight, automatically.

The morning of the appointment, your dashboard shows:
- Green: insurance verified, coverage confirmed
- Yellow: verification returned but with flags (waiting period, coverage limits, secondary insurance question)
- Red: verification failed or insurance inactive

**For yellow and red flags:** The front desk sees the flag when the patient checks in. Kasper shows what the issue is and surfaces the next step — call the insurance line, ask the patient to update their coverage, or collect as self-pay.

### 3.2 Manual Verification

For patients whose insurance couldn't be verified automatically:

1. Open the patient's chart in Kasper
2. Go to **Insurance → Verify Manually**
3. Kasper provides the insurance company's phone number and the information to have ready
4. Enter verification results — they write to the Open Dental chart

**Tip:** Build a habit of reviewing the verification dashboard every morning before the first appointment. Five minutes at 8 AM prevents a frustrated patient at checkout.

---

## Phase 4 — Payments (Day 3–4)

### 4.1 Set Up KasperPay

KasperPay is your integrated payment processor. It replaces standalone terminals and connects directly to the Open Dental ledger.

Your onboarding specialist will handle merchant account setup. Once approved (typically 1–2 business days), you receive your card terminal and can begin processing.

**At checkout:**
1. Treatment is complete
2. Front desk opens the patient's account in Kasper
3. Insurance portion is auto-calculated from the ledger
4. Patient's balance is displayed
5. Collect via terminal or send a text-to-pay link
6. Payment posts to the Open Dental ledger automatically

**Text-to-pay:** For patients who prefer to pay from their phone, or who leave before paying, send a text-to-pay link from the patient's account screen. They receive a text with a secure link, pay online, and the ledger updates in real time.

### 4.2 Set Up Payment Plans

For larger treatment balances, Kasper supports in-house payment plans:

1. Open patient account → **Payments → Create Payment Plan**
2. Set total amount, payment schedule, and card on file
3. Kasper auto-charges on the agreed date and posts each payment to the ledger

**Failed payments:** When a card on file is declined, Kasper flags it on your dashboard and sends the patient an automatic text with a link to update their payment method. You'll also receive a daily summary email listing every failed transaction.

---

## Phase 5 — Supervision Tools (Day 4–5)

### 5.1 The Intraday Dashboard (The Lobby)

This is your live view of the practice during operating hours. Keep it open on a monitor at the front desk.

Each patient who checks in appears as a card. The card shows:
- Current status (arrived, in chair, in treatment, checkout)
- Outstanding forms
- Unpaid balance
- Unscheduled treatment value
- Insurance verification status

When the card shows a flag, click it. Kasper shows you exactly what to do.

**The rule:** Do not let a patient reach checkout with an unresolved flag. Collecting payment, signing consent, and booking follow-up treatment is significantly harder once the patient leaves the building.

### 5.2 Call Intelligence

Once phones are live and Call AI is active, every call is automatically:
- Transcribed in full
- Classified by topic (scheduling, cancellation, billing, patient in pain, new patient inquiry, etc.)
- Analyzed against your governance rules (e.g., did the agent offer to reschedule after a cancellation?)
- Summarized and written to the patient's Open Dental chart

**For staff:** You don't need to take notes after calls. The summary is already in the chart.

**For managers:** Review call intelligence reports under **Reports → Call Intelligence**. You'll see every call flagged for governance issues, plus agent compliance scores. This is your coaching tool, not a surveillance tool — use it to identify training needs, not to penalize.

### 5.3 Event-Based Governance Rules

Go to **Settings → Governance Rules** to configure your office SOPs.

Example rules to set up on day one:
- Cancellation call: "Did agent offer to reschedule? If no → create task + email manager"
- Missed call: "If not returned within 1 hour → create task"
- Patient arrives with unsigned consent → flag on intraday dashboard
- Patient balance over $200 at checkout → flag for collection before exit

Each rule follows the same pattern: define the event, define the expected action, define what happens when it's missed.

You don't need to configure everything at once. Start with the two or three rules that address your biggest current pain points, then add more as the team gets comfortable.

---

## Phase 6 — Revenue Tools (Week 2)

### 6.1 Revenue Leakage Protector

Go to **Revenue → Leakage Dashboard** once your data has been syncing for several days.

The dashboard surfaces:

- **Unscheduled treatment:** patients with accepted treatment plans who never booked. Sorted by dollar value. One click to call or text them.
- **Lapsed recall patients:** patients overdue for hygiene. Kasper can send automated recall campaigns to this list.
- **Unallocated payments:** money received but not mapped to a procedure in Open Dental. Flags these for your billing coordinator to resolve.
- **Aging balances:** patient balances grouped by 30/60/90+ days. One click to send a text-to-pay link to any patient.
- **Insurance claims not yet paid:** pending claims past the expected payment window. Flags for follow-up.

Set aside 30 minutes each week to work through the leakage dashboard. For most practices, the first review surfaces several thousand dollars in recoverable revenue that was simply never followed up on.

### 6.2 Opportunity Finder

When a cancellation creates a gap in your schedule:

1. Hover over the empty slot in the Kasper schedule view
2. Select the treatment type that fits the time slot and operatory
3. Kasper scans Open Dental for patients with matching unscheduled treatment
4. Results are ranked by: remaining insurance benefits, treatment value, and appointment reliability history
5. Click a patient → call or text them directly from the Kasper interface
6. If they confirm → drag them onto the slot

**Tip:** Don't wait for a cancellation to use Opportunity Finder. Run it proactively on slow weeks to fill low-production days.

### 6.3 Recall Campaigns

Go to **Campaigns → Recall** to set up automated hygiene outreach.

For patients overdue for their 6-month cleaning, Kasper sends automated SMS and email sequences:
- First message: friendly reminder they're due
- Second message (7 days later, if no response): "We have openings this week"
- Third message (14 days later): direct link to online scheduling

You can also run manual campaigns — select all hygiene-overdue patients, filter by last visit date, and send a one-time message with a booking link.

---

## Day-to-Day Reference: Your Daily Workflow

**Morning (before first patient):**
- Review the Morning Huddle dashboard — today's production goal, scheduled vs. confirmed appointments, any open flags from yesterday
- Check the insurance verification dashboard — resolve any red and yellow flags before patients arrive
- Confirm all digital forms were sent for today's new patients

**During the day:**
- Keep the intraday dashboard open at the front desk
- Address flags on patient cards before the patient moves to checkout
- Respond to incoming texts and calls from the Kasper communication panel
- When a cancellation comes in, open Opportunity Finder immediately

**End of day:**
- Check the Revenue Leakage dashboard for any new unallocated payments or unresolved flags
- Review failed payment transactions — send text-to-pay links to any patients who owe
- Confirm tomorrow's appointment reminders have sent

---

## Support & Escalation

If something isn't working:

| Issue | First step |
|---|---|
| Open Dental sync not updating | Check database connection in Settings → Integrations. If offline, contact support. |
| Patient form not appearing in Open Dental | Check form submission status in Kasper → confirm Open Dental sync is active |
| Call popup not appearing | Confirm VoIP is active and phone extension is assigned to your Kasper user |
| Insurance verification returning errors | Check that patient's insurance info is correctly entered in Open Dental |
| Payment not posting to ledger | Check KasperPay status and Open Dental ledger permissions |
| Reminder not sent | Check patient's contact preferences in Open Dental and opt-out status in Kasper |

**Kasper Support:**
- Email: support@meetkasper.com
- Phone: (888) 312-8245
- Available during business hours, Monday–Friday

When contacting support, include: the patient name or account number (if patient-related), a screenshot if possible, and a description of what you expected to happen vs. what actually happened. This gets your issue resolved in one exchange instead of three.

---

*Prepared by Kasper Support · meetkasper.com · support@meetkasper.com*

# MURLI: Mapping 18 Types to 11 Existing Categories

## 📊 YOUR EXISTING 11 CATEGORIES

### ✅ CREATE_ACTION (5 categories)
1. Future Deadline
2. Self-Commitment
3. Meeting — Future
4. Follow-up — Future
5. Conditional Future

### 🔕 NONE (6 categories)
6. Immediate / Now
7. Past Tense — Done
8. Social / Greeting
9. FYI / Info Only
10. Vague / No Owner
11. Hard Negatives

---

## 🎯 COMPLETE MAPPING: 18 Types → 11 Categories

### ✅ CREATE_ACTION MAPPINGS

#### 1️⃣ **Future Deadline** ← Maps from:
- ✓ **Direct Requests** (with future anchor)
  - "Rahul submit report by Friday"
  - "Priya send invoice by EOD"
- ✓ **Delegations** (with future anchor)
  - "Priya you handle client call tomorrow"
  - "Arjun coordinate with vendor next week"
- ✓ **Deadline Mentions**
  - "Report due next Friday"
  - "Proposal deadline is Monday"

**Common pattern:** Named person + task + future time anchor

---

#### 2️⃣ **Self-Commitment** ← Maps from:
- ✓ **Self-Commitments**
  - "I'll send proposal by EOD"
  - "Will call client tomorrow"
- ✓ **Promises to Others**
  - "I'll get back to you by Monday"
  - "I promise to deliver by Friday"
- ✓ **Future Plans** (when speaker commits)
  - "I'm going to discuss this next week"
  - "Will review candidates on Friday"

**Common pattern:** I'll/Will + task + future time anchor

---

#### 3️⃣ **Meeting — Future** ← Maps from:
- ✓ **Meeting Announcements**
  - "Team meeting tomorrow 10am"
  - "Client call Friday 3pm on Zoom"
- ✓ **Scheduled Events**
  - "Demo scheduled for 3pm tomorrow"
  - "Training session next Wednesday"

**Common pattern:** Meeting/call/event + future time + optional location

---

#### 4️⃣ **Follow-up — Future** ← Maps from:
- ✓ **Follow-up Needed**
  - "Follow up with vendor next week"
  - "Ping client on Friday"
  - "Chase them tomorrow"
- ✓ **Soft Requests** (when follow-up emerges in thread)
  - Thread: "Can you check?" → "Sure, I'll follow up tomorrow"

**Common pattern:** Follow-up/chase/ping + person/entity + future time

---

#### 5️⃣ **Conditional Future** ← Maps from:
- ✓ **Conditional Future**
  - "Once client confirms, send contract"
  - "If they agree, schedule meeting"
  - "After approval, deploy immediately"
- ✓ **Gap Statements** (when action assigned)
  - Thread: "We haven't heard from vendor" → "I'll follow up once they respond"
- ✓ **Escalations** (when trigger-based)
  - Thread: "Client frustrated" → "If they call again, escalate to manager"

**Common pattern:** If/Once/After/When + trigger + action

---

### 🔕 NONE MAPPINGS

#### 6️⃣ **Immediate / Now** ← Maps from:
- ✓ **Implied Urgency**
  - "Do it right now"
  - "ASAP please"
  - "Send it immediately"
  - "Call him abhi"
- ✓ **Direct Requests** (immediate only)
  - "Send it now"
  - "Call client immediately"
- ✓ **Delegations** (immediate only)
  - "Priya handle this right now"

**Common pattern:** now/immediately/ASAP/abhi/ippude + no future anchor

---

#### 7️⃣ **Past Tense — Done** ← Maps from:
- ✓ **Corrections**
  - "No, I already sent it"
  - "Actually that's done"
  - "I submitted it this morning"
- ✓ **Compound Tasks** (completed)
  - "I reviewed and sent the contract"
  - "Fixed bug and deployed"
- ✓ **Direct Requests** (past tense)
  - "Rahul already submitted the report"

**Common pattern:** Past tense verbs (sent/done/submitted/completed) + no future action

---

#### 8️⃣ **Social / Greeting** ← Maps from:
- ✓ **Social / Greeting** (implicit - not in your 18)
  - "Good morning team!"
  - "Great work Priya! 👏"
  - "Happy birthday!"
  - "Thanks everyone"

**Common pattern:** Greetings, celebrations, appreciation, non-business chat

---

#### 9️⃣ **FYI / Info Only** ← Maps from:
- ✓ **Problem Statements** (when just informational)
  - "Client is unhappy"
  - "Server is slow today"
  - "Budget is tight this quarter"
- ✓ **Gap Statements** (when no action assigned)
  - "We haven't heard from vendor" (just observation)
  - "Still waiting on approval" (no next step)
- ✓ **Escalations** (when just reporting)
  - "Client called three times today" (FYI only)

**Common pattern:** Information shared with no action required from anyone

---

#### 🔟 **Vague / No Owner** ← Maps from:
- ✓ **Action Questions**
  - "Should we follow up?"
  - "Can someone handle this?"
  - "What do you think we should do?"
- ✓ **Soft Requests** (vague, no commitment)
  - "Someone should look into this"
  - "Maybe we should consider..."
- ✓ **Future Plans** (too vague)
  - "We should plan something sometime"
  - "Let's discuss eventually"
- ✓ **Problem Statements** (no clear owner)
  - "Someone needs to fix this"

**Common pattern:** No named owner AND no future time anchor = too vague to track

---

#### 1️⃣1️⃣ **Hard Negatives** ← Maps from:
- ✓ **Compound Tasks** (ambiguous cases)
  - "Review contract and let me know" (when is "let me know"?)
  - "Send invoice after checking" (when to check?)
- ✓ **Soft Requests** (edge cases)
  - "Whenever you get a chance" (no real deadline)
- ✓ **Direct Requests** (looks like task but isn't)
  - "Rahul said he'll handle it" (reporting, not assigning)
- ✓ **Action Questions** (edge cases)
  - "Should I send it now or wait?" (seeking guidance)
- ✓ **Escalations** (past tense reports)
  - "Manager handled the escalation yesterday"

**Common pattern:** Looks like a task but on closer inspection is NOT actionable

---

## 📊 COMPLETE MAPPING TABLE

| Your 18 Types | Maps To | Label | Notes |
|---------------|---------|-------|-------|
| Direct Requests | **Future Deadline** OR **Immediate / Now** | create_action OR none | Depends on time signal |
| Soft Requests | **Follow-up — Future** OR **Vague / No Owner** | create_action OR none | Thread-dependent |
| Compound Tasks | **Future Deadline** OR **Past Tense** OR **Hard Negatives** | create_action OR none | Depends on tense & clarity |
| Action Questions | **Vague / No Owner** | none | Rarely create_action |
| Delegations | **Future Deadline** OR **Immediate / Now** | create_action OR none | Depends on time signal |
| Corrections | **Past Tense — Done** | none | Always past tense |
| Implied Urgency | **Immediate / Now** | none | Always immediate |
| Gap Statements | **Conditional Future** OR **FYI / Info Only** | create_action OR none | Depends if action assigned |
| Problem Statements | **FYI / Info Only** OR **Vague / No Owner** | none | Usually just FYI |
| Escalations | **Conditional Future** OR **FYI / Info Only** | create_action OR none | Thread-dependent |
| Meeting Announcements | **Meeting — Future** | create_action | Always future meetings |
| Deadline Mentions | **Future Deadline** | create_action | Always future deadlines |
| Scheduled Events | **Meeting — Future** | create_action | Always future events |
| Future Plans | **Self-Commitment** OR **Vague / No Owner** | create_action OR none | Depends on commitment |
| Self-Commitments | **Self-Commitment** | create_action | Always with future anchor |
| Promises to Others | **Self-Commitment** | create_action | Always with future anchor |
| Conditional Future | **Conditional Future** | create_action | Always high forget risk |
| Follow-up Needed | **Follow-up — Future** | create_action | Always with future anchor |

---

## 🎯 SIMPLIFIED MAPPING SUMMARY

### CREATE_ACTION Categories:

**1. Future Deadline** ←
- Direct Requests (future)
- Delegations (future)  
- Deadline Mentions
- Compound Tasks (future)

**2. Self-Commitment** ←
- Self-Commitments
- Promises to Others
- Future Plans (with commitment)

**3. Meeting — Future** ←
- Meeting Announcements
- Scheduled Events

**4. Follow-up — Future** ←
- Follow-up Needed
- Soft Requests (thread → future)

**5. Conditional Future** ←
- Conditional Future
- Gap Statements (action assigned)
- Escalations (trigger-based)

---

### NONE Categories:

**6. Immediate / Now** ←
- Implied Urgency
- Direct Requests (immediate)
- Delegations (immediate)

**7. Past Tense — Done** ←
- Corrections
- Compound Tasks (past)
- Direct Requests (past)

**8. Social / Greeting** ←
- (Standalone - greetings, appreciation)

**9. FYI / Info Only** ←
- Problem Statements (no action)
- Gap Statements (observation only)
- Escalations (reporting only)

**10. Vague / No Owner** ←
- Action Questions
- Soft Requests (vague)
- Future Plans (too vague)

**11. Hard Negatives** ←
- Compound Tasks (ambiguous)
- Soft Requests (edge cases)
- Direct Requests (reported, not assigned)
- Action Questions (seeking guidance)

---

## 💡 KEY INSIGHTS

### Types That Split Into Multiple Categories:

**Direct Requests can be:**
- Future Deadline (if future anchor) → create_action
- Immediate / Now (if "now" signal) → none
- Past Tense (if already done) → none

**Soft Requests can be:**
- Follow-up — Future (if future emerges in thread) → create_action
- Vague / No Owner (if no commitment) → none
- Hard Negatives (edge cases) → none

**Compound Tasks can be:**
- Future Deadline (if future anchor) → create_action
- Past Tense (if completed) → none
- Hard Negatives (if ambiguous) → none

**Gap Statements can be:**
- Conditional Future (if action assigned) → create_action
- FYI / Info Only (if just observation) → none

**Escalations can be:**
- Conditional Future (if owner assigned with trigger) → create_action
- FYI / Info Only (if just reporting) → none

---

## ✅ DATASET GENERATION STRATEGY

### For Each of Your 11 Categories:

**1. Future Deadline (700 examples)**
- Source: Direct Requests (60%), Delegations (30%), Deadline Mentions (10%)

**2. Self-Commitment (600 examples)**
- Source: Self-Commitments (50%), Promises to Others (30%), Future Plans (20%)

**3. Meeting — Future (600 examples)**
- Source: Meeting Announcements (70%), Scheduled Events (30%)

**4. Follow-up — Future (500 examples)**
- Source: Follow-up Needed (80%), Soft Requests (20%)

**5. Conditional Future (400 examples)**
- Source: Conditional Future (70%), Gap Statements (20%), Escalations (10%)

**6. Immediate / Now (800 examples)**
- Source: Implied Urgency (70%), Direct Requests immediate (20%), Delegations immediate (10%)

**7. Past Tense — Done (600 examples)**
- Source: Corrections (40%), Compound Tasks past (40%), Direct Requests past (20%)

**8. Social / Greeting (500 examples)**
- Source: Pure social messages (100% authentic collection needed)

**9. FYI / Info Only (450 examples)**
- Source: Problem Statements (60%), Gap Statements (30%), Escalations (10%)

**10. Vague / No Owner (350 examples)**
- Source: Action Questions (50%), Soft Requests vague (30%), Future Plans vague (20%)

**11. Hard Negatives (450 examples)**
- Source: Compound Tasks ambiguous (40%), Soft Requests edge (30%), Mixed (30%)

---

## 🎯 FINAL ANSWER

**Your 18 types are NOT new categories.**  
**They are INPUT PATTERNS that map into your existing 11 categories.**

The same type (e.g., "Direct Requests") can produce examples for:
- ✅ Future Deadline (if future anchor)
- 🔕 Immediate / Now (if "now" signal)
- 🔕 Past Tense (if already done)

**Use the 18 types as TEMPLATES for generating examples.**  
**Use the 11 categories as your FINAL LABELS for training.**

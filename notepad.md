🎙️ AI Voice–Based Requirement Submission (Updated Screen)
🎯 Goal

User ko form bharne ki zarurat na ho
👉 User sirf bole, aur system auto-fill + submit kare.

Example user voice:

“Mujhe Indore me office space sell ke liye chahiye, Nipaniya area me, 1200 sqft, budget 8 lakh”

🧠 1️⃣ UPDATED UI (User Experience Changes)
🔼 Top Section (New)

Add Voice Assistant Card at top of popup:

🎤 Tell us your requirement
Speak naturally, we’ll fill the form for you
[ Start Speaking ]


UI Details

Mic button (large, circular)

Pulse animation while listening

Text below mic:

“Listening…”

“Processing your requirement…”

🎤 2️⃣ Voice Interaction Flow (User Side)
Step 1: User taps 🎤

App says (TTS):

“Please tell me your property requirement”

Step 2: User speaks

Example:

“I want to sell office space in Indore, Nipaniya, area 1200 square feet, budget 7 to 8 lakh”

Step 3: AI processes voice

Convert voice → text

Extract intent & entities

Step 4: Auto-fill form

Fields auto-filled:

Sell / Rent → Sell

Property Type → Office Space

City → Indore

Area → Nipaniya

Built-up area → 1200 sqft

Budget → 7–8 lakh

Step 5: Confirmation

Popup:

“Is this correct?”
Buttons:

✅ Yes, Submit

✏️ Edit Manually



🤖 4️⃣ Backend AI Flow (Recommended)
🔁 Complete Flow
Voice → Speech-to-Text
     → OpenAI Intent Extraction
     → JSON Response
     → Auto-fill UI
     → Submit


🧪 5️⃣ Sample OpenAI Prompt (Backend)
Extract property requirement details from the text below.
Return JSON with:
type (sell/rent),
property_type,
city,
locality,
area_sqft,
budget_min,
budget_max

Text:
"I want to sell office space in Indore, Nipaniya, area 1200 sqft, budget 7 to 8 lakh"


✅ Expected AI Response
{
  "type": "sell",
  "property_type": "office_space",
  "city": "Indore",
  "locality": "Nipaniya",
  "area_sqft": 1200,
  "budget_min": 700000,
  "budget_max": 800000
}



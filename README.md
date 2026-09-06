# medicine-recommender- 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>MedGuide - Medicine Information</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #e8f7ff, #f4f1ff);
      color: #172033;
    }

    header {
      background: linear-gradient(135deg, #1769aa, #673ab7);
      color: white;
      padding: 35px 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 42px;
    }

    header p {
      font-size: 18px;
      margin-bottom: 0;
    }

    .container {
      width: 90%;
      max-width: 900px;
      margin: 30px auto;
    }

    .warning {
      background: #fff3cd;
      border-left: 6px solid #ffb300;
      padding: 18px;
      border-radius: 10px;
      margin-bottom: 25px;
    }

    .card {
      background: white;
      padding: 25px;
      border-radius: 16px;
      margin-bottom: 25px;
      box-shadow: 0 8px 25px rgba(0,0,0,0.08);
    }

    h2 {
      color: #1769aa;
    }

    label {
      display: block;
      font-weight: bold;
      margin: 15px 0 8px;
    }

    select,
    input {
      width: 100%;
      padding: 13px;
      border: 2px solid #ddd;
      border-radius: 8px;
      font-size: 16px;
    }

    button {
      width: 100%;
      margin-top: 20px;
      padding: 15px;
      border: none;
      border-radius: 9px;
      background: #1769aa;
      color: white;
      font-size: 18px;
      font-weight: bold;
      cursor: pointer;
    }

    button:hover {
      background: #0d4f82;
    }

    #result {
      display: none;
      border-left: 6px solid #1769aa;
    }

    .medicine {
      background: #eef7ff;
      padding: 18px;
      border-radius: 10px;
      margin-top: 15px;
    }

    .medicine h3 {
      margin-top: 0;
      color: #1769aa;
    }

    .danger {
      background: #ffe8e8;
      border-left: 5px solid #e53935;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
    }

    .safe {
      background: #e8f8ef;
      border-left: 5px solid #2e9d58;
      padding: 15px;
      border-radius: 8px;
      margin-top: 15px;
    }

    footer {
      text-align: center;
      padding: 30px;
      color: #555;
    }

    @media (max-width: 600px) {

      header h1 {
        font-size: 30px;
      }

      .container {
        width: 94%;
      }

      .card {
        padding: 18px;
      }
    }
  </style>
</head>

<body>

<header>
  <h1>💊 MedGuide</h1>
  <p>Simple medicine information for common symptoms</p>
</header>

<div class="container">

  <div class="warning">

    <strong>⚠️ Important:</strong>

    This website provides general health information.
    It does NOT diagnose illnesses, prescribe medicines,
    or determine the correct dose for you.

    Always read the medicine label and ask a doctor or
    pharmacist if you are unsure.

  </div>


  <div class="card">

    <h2>🔎 Find Information</h2>

    <label for="symptom">
      What symptom are you asking about?
    </label>

    <select id="symptom">

      <option value="">
        -- Choose a symptom --
      </option>

      <option value="headache">
        🤕 Headache
      </option>

      <option value="fever">
        🌡️ Fever
      </option>

      <option value="cold">
        🤧 Cold / Runny Nose
      </option>

      <option value="cough">
        😷 Cough
      </option>

      <option value="sorethroat">
        🗣️ Sore Throat
      </option>

      <option value="acidity">
        🔥 Occasional Heartburn
      </option>

      <option value="allergy">
        🤧 Allergy Symptoms
      </option>

      <option value="diarrhea">
        💧 Diarrhea
      </option>

    </select>


    <label for="age">
      Age group
    </label>

    <select id="age">

      <option value="adult">
        Adult
      </option>

      <option value="child">
        Child
      </option>

      <option value="older">
        Older adult
      </option>

    </select>


    <button onclick="recommend()">
      🔍 Show Information
    </button>

  </div>


  <div class="card" id="result">

    <h2 id="resultTitle"></h2>

    <p id="description"></p>

    <div class="medicine">

      <h3>💊 Common medicine category</h3>

      <p id="medicineInfo"></p>

    </div>


    <div class="safe">

      <strong>✅ Safety reminder</strong>

      <p id="safety"></p>

    </div>


    <div class="danger">

      <strong>🚨 Get medical help if:</strong>

      <p id="danger"></p>

    </div>

  </div>


  <div class="card">

    <h2>🛡️ Medicine Safety</h2>

    <ul>

      <li>
        Do not take someone else's prescription medicine.
      </li>

      <li>
        Follow the directions on the medicine label.
      </li>

      <li>
        Check the active ingredients to avoid accidentally
        taking the same ingredient in multiple products.
      </li>

      <li>
        Tell your doctor or pharmacist about other medicines
        and supplements you take.
      </li>

      <li>
        Ask a healthcare professional about medicines for
        children, pregnancy, breastfeeding, or complex
        medical conditions.
      </li>

    </ul>

  </div>

</div>


<footer>

  <p>
    MedGuide is an educational project and is not a
    substitute for professional medical advice.
  </p>

  <p>
    💙 Stay safe. Ask a healthcare professional when unsure.
  </p>

</footer>


<script>

const information = {

  headache: {

    title: "🤕 Headache",

    description:
      "Many mild headaches can have causes such as stress, dehydration, lack of sleep, or a viral illness.",

    medicine:
      "For some adults, common over-the-counter pain-relief medicines may be used according to their label. Examples of medicine categories include acetaminophen/paracetamol or NSAIDs such as ibuprofen. The right choice depends on the person and their health history.",

    safety:
      "Check the active ingredients and follow the package directions. Some pain medicines may not be suitable for people with certain medical conditions or who take certain medicines.",

    danger:
      "A sudden extremely severe headache, headache after a serious injury, confusion, weakness, fainting, seizure, or headache with other serious symptoms requires urgent medical evaluation."

  },


  fever: {

    title: "🌡️ Fever",

    description:
      "Fever can occur with infections and other conditions. Treating the underlying cause is important.",

    medicine:
      "Some people use OTC fever-reducing medicines such as acetaminophen/paracetamol or ibuprofen. Whether these are appropriate depends on age, health conditions, other medicines, and the product label.",

    safety:
      "Never guess a child's medicine dose. Use the product's age/weight instructions and ask a pediatrician or pharmacist when uncertain.",

    danger:
      "Seek medical attention for severe illness, difficulty breathing, confusion, dehydration, seizure, or a concerning fever in a very young child."

  },


  cold: {

    title: "🤧 Cold / Runny Nose",

    description:
      "Common colds are usually viral and often improve with rest and supportive care.",

    medicine:
      "Depending on symptoms, OTC products may include saline nasal products, throat soothing products, or certain cold medicines. Combination products can contain multiple active ingredients.",

    safety:
      "Avoid taking multiple cold medicines without checking their active ingredients, because you may accidentally duplicate an ingredient.",

    danger:
      "Seek medical help for trouble breathing, severe dehydration, persistent severe symptoms, or symptoms that are getting significantly worse."

  },


  cough: {

    title: "😷 Cough",

    description:
      "Coughs can occur with colds, allergies, asthma, infections, and many other conditions.",

    medicine:
      "Some OTC cough products are available, but the appropriate product depends on the type and cause of the cough.",

    safety:
      "Do not give cough or cold medicines to young children unless a healthcare professional recommends them.",

    danger:
      "Get urgent medical help for difficulty breathing, coughing blood, blue lips, severe chest pain, or serious worsening symptoms."

  },


  sorethroat: {

    title: "🗣️ Sore Throat",

    description:
      "A sore throat commonly occurs with viral infections but can have other causes.",

    medicine:
      "Supportive options can include fluids, warm beverages, throat lozenges, and appropriate OTC pain-relief products.",

    safety:
      "Antibiotics should not be taken unless prescribed for an appropriate bacterial infection.",

    danger:
      "Seek medical care for difficulty breathing or swallowing, severe swelling, dehydration, or rapidly worsening symptoms."

  },


  acidity: {

    title: "🔥 Occasional Heartburn",

    description:
      "Occasional heartburn can happen when stomach acid moves upward into the esophagus.",

    medicine:
      "Some OTC antacid and acid-reducing medicine categories can provide short-term relief. A pharmacist can help identify an appropriate option.",

    safety:
      "If heartburn happens frequently, do not simply keep taking OTC medicine without discussing it with a healthcare professional.",

    danger:
      "Chest pressure or pain with sweating, shortness of breath, dizziness, or pain spreading to the arm or jaw requires urgent medical evaluation."

  },


  allergy: {

    title: "🤧 Allergy Symptoms",

    description:
      "Allergies can cause symptoms such as sneezing, itchy eyes, and a runny nose.",

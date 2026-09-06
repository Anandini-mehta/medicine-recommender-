# medicine-recommender- 
<!DOCTYPE html> <html lang="en"> <head> <meta charset="UTF-8">
<meta name="viewport"
      content="width=device-width, initial-scale=1.0">

<meta name="description"
      content="Medicine Recommender - General health information based on symptoms">

<title>MedGuide - Medicine Recommender</title>

<link rel="stylesheet" href="./style.css">

</head> <body> <header class="navbar">
<div class="logo">
    <span>✚</span>
    MedGuide
</div>

<nav>
    <a href="#home">Home</a>
    <a href="#recommender">Recommender</a>
    <a href="#medicines">Medicines</a>
    <a href="#about">About</a>
</nav>

</header> <main> <!-- HERO --> <section id="home" class="hero">
<div class="hero-content">

    <div class="badge">
        🩺 Smart Health Assistant
    </div>

    <h1>
        Find General Medicine
        <span>Information</span>
    </h1>

    <p>
        Select your symptoms and get general information
        about commonly used medicines and health precautions.
    </p>

    <a href="#recommender" class="hero-button">
        Start Recommender →
    </a>

</div>

<div class="hero-card">

    <div class="doctor-icon">
        🧑‍⚕️
    </div>

    <h3>
        Health Information
    </h3>

    <p>
        Simple, fast and easy to use.
    </p>

    <div class="health-stat">
        <strong>20+</strong>
        <span>Symptoms</span>
    </div>

    <div class="health-stat">
        <strong>15+</strong>
        <span>Medicine entries</span>
    </div>

</div>

</section> <!-- RECOMMENDER --> <section id="recommender" class="section">
<div class="section-title">

    <span>01</span>

    <div>
        <h2>Medicine Recommender</h2>

        <p>
            Tell us what symptoms you are experiencing.
        </p>
    </div>

</div>


<div class="recommender-box">

    <div class="input-area">

        <label>
            Search symptoms
        </label>

        <div class="search-input">

            <span>🔎</span>

            <input
                type="text"
                id="symptomInput"
                placeholder="Type a symptom..."
                autocomplete="off"
            >

        </div>


        <div class="suggestions">

            <button data-symptom="fever">
                Fever
            </button>

            <button data-symptom="headache">
                Headache
            </button>

            <button data-symptom="cough">
                Cough
            </button>

            <button data-symptom="cold">
                Cold
            </button>

            <button data-symptom="allergy">
                Allergy
            </button>

            <button data-symptom="acidity">
                Acidity
            </button>

            <button data-symptom="stomach pain">
                Stomach Pain
            </button>

            <button data-symptom="

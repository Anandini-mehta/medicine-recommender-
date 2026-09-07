# medicine-recommender- 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Disease Researcher</title>

<style>

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    background: #f1f5f9;
    color: #172033;
}

/* HEADER */

header {
    background: linear-gradient(135deg, #075985, #2563eb);
    color: white;
    padding: 45px 20px;
}

.header-container {
    max-width: 1100px;
    margin: auto;
}

header h1 {
    margin: 0;
    font-size: 42px;
}

header p {
    font-size: 18px;
    margin-top: 10px;
}

/* MAIN */

main {
    max-width: 1100px;
    margin: 30px auto;
    padding: 0 20px;
}

/* DISCLAIMER */

.disclaimer {
    background: #fff7ed;
    border-left: 5px solid #f97316;
    padding: 18px;
    border-radius: 8px;
    margin-bottom: 25px;
}

/* TABS */

.tabs {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
}

.tab {
    border: none;
    padding: 14px 22px;
    border-radius: 8px;
    background: #dbeafe;
    color: #1e3a8a;
    font-size: 16px;
    cursor: pointer;
}

.tab.active {
    background: #2563eb;
    color: white;
}

/* CARD */

.card {
    background: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.06);
    margin-bottom: 25px;
}

.card h2 {
    margin-top: 0;
}

/* INPUTS */

input,
textarea {
    width: 100%;
    padding: 15px;
    border: 1px solid #cbd5e1;
    border-radius: 8px;
    font-size: 16px;
    margin-bottom: 15px;
    outline: none;
}

textarea {
    min-height: 130px;
    resize: vertical;
}

input:focus,
textarea:focus {
    border-color: #2563eb;
}

/* BUTTON */

.primary-button {
    background: #2563eb;
    color: white;
    border: none;
    padding: 14px 22px;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
}

.primary-button:hover {
    background: #1d4ed8;
}

/* RESULTS */

#results {
    display: none;
}

.result-section {
    background: white;
    padding: 25px;
    margin-bottom: 18px;
    border-radius: 10px;
    border-left: 4px solid #2563eb;
}

.result-section h2 {
    color: #075985;
    margin-top: 0;
}

.result-section h3 {
    color: #334155;
}

.result-section ul {
    padding-left: 25px;
}

.result-section li {
    margin-bottom: 7px;
}

/* WARNING */

.warning {
    background: #fee2e2;
    border-left: 5px solid #dc2626;
    padding: 18px;
    border-radius: 8px;
    margin-bottom: 20px;
}

/* SUCCESS */

.success {
    background: #dcfce7;
    border-left: 5px solid #16a34a;
    padding: 18px;
    border-radius: 8px;
}

/* HIDDEN */

.hidden {
    display: none;
}

/* FOOTER */

footer {
    text-align: center;
    padding: 30px;
    color: #64748b;
}

/* MOBILE */

@

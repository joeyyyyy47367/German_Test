# German_Test
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Sydney's Mini Deutsch-Test 🦝</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; max-width: 800px; margin: auto; background: #f9f9f9; }
    h1 { color: #333; }
    .question { margin-bottom: 20px; }
    button { padding: 10px 20px; cursor: pointer; background-color: #4CAF50; color: white; border: none; }
    #result { margin-top: 30px; font-size: 18px; }
  </style>
</head>
<body>

<h1>🦝 Sydney's Mini Deutsch-Test 🦝</h1>

<form id="quizForm">

  <div class="question">
    <p>1️⃣ Wo ist Joe? 🧐</p>
    <input type="radio" name="q1" value="a"> a) Joe ist in Birmingham.<br>
    <input type="radio" name="q1" value="b"> b) Joe ist in Rottenburg.<br>
    <input type="radio" name="q1" value="c"> c) Joe ist im Kühlschrank.<br>
  </div>

  <div class="question">
    <p>2️⃣ Wer ist Flabio? 🦝</p>
    <input type="radio" name="q2" value="a"> a) Flabio ist ein Waschbär.<br>
    <input type="radio" name="q2" value="b"> b) Flabio ist ein Lehrer.<br>
    <input type="radio" name="q2" value="c"> c) Flabio ist ein Auto.<br>
  </div>

  <div class="question">
    <p>3️⃣ Sydney geht nach Rottenburg. Warum? 💃</p>
    <input type="radio" name="q3" value="a"> a) Er will Joe sehen.<br>
    <input type="radio" name="q3" value="b"> b) Er will tanzen.<br>
    <input type="radio" name="q3" value="c"> c) Er will schlafen.<br>
  </div>

  <div class="question">
    <p>4️⃣ Wie sagt man „Hello, I am Sydney“ auf Deutsch? 👋</p>
    <input type="radio" name="q4" value="a"> a) Hallo, ich bin Sydney.<br>
    <input type="radio" name="q4" value="b"> b) Hallo, ich heißt Sydney.<br>
    <input type="radio" name="q4" value="c"> c) Hallo, ich habe Sydney.<br>
  </div>

  <div class="question">
    <p>5️⃣ Wer ist böse auf die Flughafen-Security? ✈️</p>
    <input type="radio" name="q5" value="a"> a) Sydney hat einen Koffer bei der Security.<br>
    <input type="radio" name="q5" value="b"> b) Sydney und Joe sind böse auf die Security.<br>
    <input type="radio" name="q5" value="c"> c) Sydney und Joe lieben die Security.<br>
  </div>

  <div class="question">
    <p>6️⃣ Was macht Flabio in Birmingham? 🎉</p>
    <input type="radio" name="q6" value="a"> a) Flabio tanzt im Club.<br>
    <input type="radio" name="q6" value="b"> b) Flabio schläft in Joe’s Koffer.<br>
    <input type="radio" name="q6" value="c"> c) Flabio arbeitet als Security.<br>
  </div>

  <div class="question">
    <p>7️⃣ Was sagt Sydney im Restaurant? 🍽️</p>
    <input type="radio" name="q7" value="a"> a) Ich möchte bitte einen Kaffee.<br>
    <input type="radio" name="q7" value="b"> b) Ich bin ein Waschbär.<br>
    <input type="radio" name="q7" value="c"> c) Wo ist Flabio?<br>
  </div>

  <button type="button" onclick="checkAnswers()">Ergebnis anzeigen</button>
</form>

<div id="result"></div>

<script>
function checkAnswers() {
  const correctAnswers = { q1: "b", q2: "a", q3: "a", q4: "a", q5: "b", q6: "a", q7: "a" };
  let score = 0;
  let feedback = "";

  for (let q in correctAnswers) {
    const userAnswer = document.querySelector(`input[name="${q}"]:checked`);
    if (userAnswer) {
      if (userAnswer.value === correctAnswers[q]) {
        score++;
        feedback += `✅ Frage ${q.slice(1)} richtig!<br>`;
      } else {
        feedback += `❌ Frage ${q.slice(1)} falsch.<br>`;
      }
    } else {
      feedback += `⚠️ Frage ${q.slice(1)} nicht beantwortet.<br>`;
    }
  }

  document.getElementById("result").innerHTML = `
    <h2>Dein Ergebnis: ${score}/7</h2>
    ${feedback}
    ${score >= 5 ? "🎉 Super gemacht, Sydney! Weiter so!" : "💪 Üben wir noch ein bisschen, du schaffst das!"}
  `;
}
</script>

</body>
</html>

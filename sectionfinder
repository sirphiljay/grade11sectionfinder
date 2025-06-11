<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Student Section Finder</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 600px;
      margin: 40px auto;
      padding: 20px;
    }
    input {
      width: 100%;
      padding: 10px;
      font-size: 1rem;
      margin-bottom: 20px;
    }
    #result {
      border-top: 1px solid #ccc;
      padding-top: 20px;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>
  <h2>Student Section Finder</h2>
  <input type="text" id="searchInput" placeholder="Enter your full name..." />
  <div id="result"></div>

  <script>
    const students = [
      { name: "Almonte Kevin James", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Apura Lourence", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Baang Kent Nathaniele", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Bacon Denielle Jake", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Dayanan Cristof", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Fernandez John Mark", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Gako Christian", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Irona Dave", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Lauron Christian", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Lausa BB Jenboy", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Lu-ang Richard Dems", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Pantilgan Jackris", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Remo Criss Michol", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Satinitigan June Vincent", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Tangaro Negro Patrick", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Tumulak Kienneth", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Ygona Ansel", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Amistad Mary Cris", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Cabungcal Nechel Mae", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Cabungcal Krisha Marie", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Dela Cerna Samantha", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Enad Sweet Kiel", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Erezo Kristel", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Espinosa Angelie", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Larrobis Glyza Mar", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Lauron Shane", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Legarte Jhilia Mie", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Liniojan Beverly", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Mortifero Shane", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Navarro Chiecky Jayne", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Naveo Maria Ivonne", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Navoa Kisha Mae", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Pansan Fhebe Gail", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Parame Kylla", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Rudila Zairra", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Sabala Rhia Madjih", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },
      { name: "Tangaro Ella Mae", section: "Grade 11 - Aristotle", adviser: "Mr. Phil Jay M. Duangon" },

      // Socrates
      { name: "Baculpo John Mike", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Satinitigan Rendy", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Siboco John Lenard", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Lauron Brian", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Aldaya Bhorly", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Ybañez Vaughn Uriel", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Fernandez John Lloyd", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Rim Raven", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      { name: "Lausa John Khyl", section: "Grade 11 - Socrates", adviser: "Mr. Clemente A. Villacastin, Jr." },
      // ... Add the rest of Socrates students here in the same format
    ];

    document.getElementById("searchInput").addEventListener("input", function () {
      const query = this.value.trim().toLowerCase();
      const resultDiv = document.getElementById("result");

      if (!query) {
        resultDiv.textContent = "";
        return;
      }

      const student = students.find(s => s.name.toLowerCase() === query);

      if (student) {
        resultDiv.innerHTML = `
          <strong>Student Name:</strong> ${student.name}<br>
          <strong>Section:</strong> ${student.section}<br>
          <strong>Class Adviser:</strong> ${student.adviser}
        `;
      } else {
        resultDiv.innerHTML = `No record found for "${this.value}". Please check the spelling.`;
      }
    });
  </script>
</body>
</html>

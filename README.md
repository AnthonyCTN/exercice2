# exercice2
ecercice 2 EXERCICE 2 : PERSONNE AGES v2.




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1><u> EXERCICE 2 : PERSONNE AGES v2.</u></h1>

  <form id="ageForm">
    <label for="age1">Âge 1 :</label>
    <input type="number" id="age1" required><br>

    <label for="age2">Âge 2 :</label>
    <input type="number" id="age2" required><br>

    <label for="age3">Âge 3 :</label>
    <input type="number" id="age3" required><br>

    <label for="age4">Âge 4 :</label>
    <input type="number" id="age4" required><br>

    <label for="age5">Âge 5 :</label>
    <input type="number" id="age5" required><br>

    <button type="submit">Vérifier</button>
  </form>

  <div id="result"></div>



    <script>
           document.getElementById("ageForm").addEventListener("submit", function(event) {
      event.preventDefault()


      #The code retrieves the values from five HTML input elements representing ages and converts them to integers using the parseInt() function.

      var age1 = parseInt(document.getElementById("age1").value);
      var age2 = parseInt(document.getElementById("age2").value);
      var age3 = parseInt(document.getElementById("age3").value);
      var age4 = parseInt(document.getElementById("age4").value);
      var age5 = parseInt(document.getElementById("age5").value);

      var countMinors = 0;


      #The code uses a switch statement to check if each of the five age variables is less than 18. If an age is less than 18, the countMinors variable is incremented. The switch statement allows for multiple cases to be executed sequentially if they meet the condition.

      switch (true) {
        case age1 < 18:
          countMinors++;
        case age2 < 18:
          countMinors++;
        case age3 < 18:
          countMinors++;
        case age4 < 18:
          countMinors++;
        case age5 < 18:
          countMinors++;
      }

      var result = document.getElementById("result");

#The code uses a switch statement to determine the value of the countMinors variable and sets the text content of the "result" element accordingly, providing different messages based on the count of minors (0, 1, or more than 1)


      switch (countMinors) {
        case 0:
          result.textContent = "Il n'y a pas de mineurs";
          break;
        case 1:
          result.textContent = "Il y a un seul mineur";
          break;
        default:
          result.textContent = "Il y a au moins deux mineurs";
          break;
      }
    });
  </script>
    </script>
</body>
</html>

<style>
   body {
  font-family: Arial, sans-serif;
}

form {
  max-width: 600px;
  margin: 0 auto;
}

label, input {
  display: block;
  width: 100%;
  margin-bottom: 20px;
}

input[type="number"] {
  padding: 10px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #101010;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #3e3c3c;
}

@media (max-width: 600px) {
  label, input {
    width: 100%;
  }
}

#result {

    text-align: center;
  margin: 20px auto;
  max-width: 600px;
  color: green;
}
h1{
    text-align: center;
}
  </style>

<!DOCTYPE html>
<html>
<head>
  <title>Παρουσία Μαθήματος</title>
  <script>
    // Συνάρτηση για τη λήψη γεωγραφικής θέσης
    function getLocation() {
      if (navigator.geolocation) {
        // Αν η γεωεντοπισμός υποστηρίζεται, καλέστε τη συνάρτηση showPosition
        navigator.geolocation.getCurrentPosition(showPosition);
      } else {
        alert("Η γεωγραφική τοποθεσία δεν υποστηρίζεται από αυτό το πρόγραμμα περιήγησης.");
      }
    }

    // Αυτή η συνάρτηση θα εκτελείται όταν η γεωγραφική θέση ληφθεί επιτυχώς
    function showPosition(position) {
      // Γεωγραφικό πλάτος και μήκος από την τοποθεσία του χρήστη
      document.getElementById('latitude').value = position.coords.latitude;
      document.getElementById('longitude').value = position.coords.longitude;

      // Αυτόματη υποβολή της φόρμας
      document.getElementById('myForm').submit();
    }
  </script>
</head>
<body onload="getLocation()">
  <h1>Παρουσία Μαθήματος</h1>
  <!-- Η φόρμα που ενσωματώνει το Google Form -->
  <form id="myForm" action="https://docs.google.com/forms/d/e/FORM_ID_HERE/formResponse" method="POST">
    <label>Όνομα:</label>
    <input type="text" name="entry.XXXXX" required><br>
    <input type="hidden" id="latitude" name="entry.YYYYY">
    <input type="hidden" id="longitude" name="entry.ZZZZZ">
    <label>Email:</label>
    <input type="email" name="entry.WWWWW"><br>
    <input type="submit" value="Υποβολή">
  </form>
</body>
</html>

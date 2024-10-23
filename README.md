<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Παρουσία Μαθήματος</title>
</head>
<body>
    <h1>Φόρμα Παρουσίας Μαθήματος</h1>
    <form id="attendanceForm">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required><br><br>
        
        <label for="latitude">Γεωγραφικό πλάτος:</label>
        <input type="text" id="latitude" name="latitude" readonly><br><br>
        
        <label for="longitude">Γεωγραφικό μήκος:</label>
        <input type="text" id="longitude" name="longitude" readonly><br><br>
        
        <button type="submit">Υποβολή Παρουσίας</button>
    </form>

    <script>
        // Λειτουργία για λήψη γεωγραφικής τοποθεσίας
        navigator.geolocation.getCurrentPosition(function(position) {
            document.getElementById('latitude').value = position.coords.latitude;
            document.getElementById('longitude').value = position.coords.longitude;
        });
    </script>
</body>
</html>
    <input type="email" name="entry.552637671"><br>
    <input type="submit" value="Υποβολή">
  </form>
</body>
</html>


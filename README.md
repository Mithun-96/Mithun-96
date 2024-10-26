<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Admission Form</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-image: url('background-image.jpg'); /* Replace with your image URL */
            background-size: cover;
            background-position: center;
            margin: 0;
            padding: 20px;
            color: #333;
        }
        h1 {
            color: #000000;
            text-align: center;
            margin-bottom: 20px;
        }
        form {
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            max-width: 600px;
            margin: auto;
        }
        label {
            display: block;
            margin: 15px 0 5px;
            color: #555;
        }
        input[type="text"],
        input[type="number"],
        select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 15px;
            transition: border-color 0.3s;
        }
        input[type="text"]:focus,
        input[type="number"]:focus,
        select:focus {
            border-color: #007bff;
            outline: none;
        }
        input[type="submit"] {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
            width: 100%;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
        .gender-checkbox {
            display: inline-block;
            margin-right: 15px;
        }
        .alert {
            color: red;
            font-weight: bold;
        }
        @media (max-width: 768px) {
            form {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
  <img src="Ca.png" alt="Christ academy logo">
  <h1>Admission Form </h1>
    
    <form action="/action_page.php">
        
      <label for="fname">Student name:</label>
        <input type="text" id="fname" name="fname"><br><br>
       
        <h4>Date of birth</h4>
        <input type="datetime-local" 
               id="Test_DatetimeLocal">
        <br><br>

        <h4>Gender-checkbox</h4>
 <input type="checkbox" id="male" name="male" value="male">
  <label for="male">Male</label><br>
  <input type="checkbox" id="female" name="female" value="female">
  <label for="female">female</label><br>
        
        <label for="blood group">Blood group:</label>
        <input type="text" id="blood group" name="blood group"><br><br>

        <label for="address">Address:</label>
        <input type="text" id="address" name="address"><br><br>

        <label for="Aadhar no">Aadhar no:</label>
        <input type="text" id="Aadhar no" name="Aadhar no"><br><br>
        
<label for="grade">Choose a grade:</label>
        <select name="grade" id="grade">
          <option value="prekg">Prekg</option>
          <option value="LKG">LKG</option>
          <option value="UKG">UKG</option>
          <option value="1">1</option>
           <option value="2">2</option>
            <option value="3">3</option>
          <option value="4">4</option>
          <option value="5">5</option>
          <option value="6">6</option>
           <option value="7">7</option> 
           <option value="8">8</option>
          <option value="9">9</option>
          <option value="10">10</option>
          <option value="11">11</option>
           <option value="12">12</option> 
</select><br><br>
  
<script>
  document.getElementById('grade').addEventListener("change", function() {
    if (this.value === 'prekg') {
      alert('New Admission');
    } else {
      myFunction(); // Call the function to prompt for previous school
    }
  });

  function myFunction() {
    let person = prompt("Previous school", "");
    if (person != null) {
      // Display the previous school name in the demo div
      document.getElementById("demo").innerHTML = "Previous school: " + person;
    }
  }
</script>

<p> Click here to upload the photo<p>
  
  <video id="video" autoplay></video>
  <canvas id="canvas" style="display:none;"></canvas>
  <button id="capture">Capture Photo</button>
  <img id="photo" alt="Captured Photo"/>
  
  <script>
    const video = document.getElementById('video');
    const canvas = document.getElementById('canvas');
    const photo = document.getElementById('photo');
    const captureButton = document.getElementById('capture');
  
    // Access the user's camera
    navigator.mediaDevices.getUserMedia({ video: true })
      .then((stream) => {
        video.srcObject = stream;
      })
      .catch((err) => {
        console.error('Error accessing camera: ', err);
      });
  
    // Capture photo on button click
    captureButton.addEventListener('click', () => {
      canvas.width = video.videoWidth;
      canvas.height = video.videoHeight;
      canvas.getContext('2d').drawImage(video, 0, 0);
      photo.src = canvas.toDataURL('image/png');
    });
  </script>

<br><br><label for="dadname">Father's name:</label>
        <input type="text" id="dadname" name="dadname"><br><br>

        <label for="momname">Mother's name:</label>
        <input type="text" id="momname" name="momname"><br><br>

<label for="dadjob">Father's Occupation:</label>
        <input type="text" id="dadjob" name="dadjob"><br><br>

        <label for="momjob">Mother's Occupation:</label>
        <input type="text" id="momjob" name="momjob"><br><br>

        <label for="dadqualification">Father's Qualification:</label>
        <input type="text" id="dadqualification" name="dadqualification"><br><br>

        <label for="momqualification">Mother's Qualification:</label>
        <input type="text" id="momqualification" name="momqualification"><br><br>

        <label for="dadmobno">Father's Mobile No.:</label>
        <input type="number" id="dadmobno" name="dadmobno"><br><br>

        <label for="mommobno">Mother's Mobile No.:</label>
        <input type="number" id="mommobno" name="mommobno"><br><br>

         <label for="dadoffno">Father's Office Mobile No.:</label>
        <input type="number" id="dadoffno" name="dadoffno"><br><br>

        <label for="momoffno">Mother's Office Mobile No.:</label>
        <input type="number" id="momoffno" name="momoffno"><br><br>

         <label for="dademail">Father's E-mail:</label>
        <input type="text" id="dademail" name="dademail"><br><br>

        <label for="momemail">Mother's E-mail:</label>
        <input type="text" id="momemail" name="momemail"><br><br>

         <input type="submit" value="Submit">
</form>
</body>
</html>

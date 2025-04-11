# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

ANSWERS:
HTML
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="style.css" />
  <title>Browser</title>
</head>

<body>
  <ol class="cotainer" type="I">
    <li>HTML</li>
    <li>CSS</li>
    <li>JS</li>
  </ol>
  <img scr="https://www.pexels.com/photo/a-young-woman-in-a-green-jacket-sitting-and-holding-a-fujifilm-x100f-digital-camera-20570035/" alt="Beautiful" width="500">
    <table>
      <tr>
        <th>Name</th>
        <th>Address</th>
        <th>Mobile</th>
        <th>Email</th>
      </tr>
      <tr>
        <td>Agbo Samson</td>
        <td>Enugu state, Nigera</td>
        <td>07035946121</td>
        <td>agbo4samson@gmail.com</td>
      </tr>
    </table>
    
    <fieldset>
      <legend>Registration form</legend>
      <label for="name">Name:</label>
      <input type="text" id="username" name"username" placeholder="Enter your full name" required><br><br>
      <label for="password">Password:</label>
      <input type="password" id="password" name="password" maxlength="8"><br><br>
      <label for="dob">DOB:</label>
      <input type="date" id="dob" name="dob" min="1990-01-01" max="2013-01-01" required><br><br>
      <label for="country">Country:</label>
      <select id="country" name="country">
        <option value="">Country</option>
        <option value="1">Nigeria</option>
        <option value="2">United State</option>
        <option value="3">United Kingdom</option>
        <option value="4">Southern Africa</option>
      </select><br><br>
        <label for="Gender">Gender:</label><br>
        <input type="radio" id="male" name="gender" value="male">
          <label for="male">Male</label>
          <input type="radio" id="female" value="female">
          <label for="male">Female</label>
        
            <p>Kidly confirm that the above details are true about you</p>
            <input type="checkbox" id="affirmation" value="affirmation">
    </fieldset>
     <audio controls>
              <source src="https://audiomack.com/eriggapaperboi/album/goat">
                Your browser does not support the audio format
     </audio>
       <video controls width="300">
         <source src="https://www.youtube.com/watch?v=vVFXsk0n24o">
           Your browser does not support the video format
       </video>
        
</body>

</html>

CSS

body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      box-sizing: border-box;
    }

    ol {
      padding-left: 20px;
    }

    img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 20px 0;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
    }

    th, td {
      border: 1px solid #333;
      padding: 10px;
      text-align: left;
    }

    fieldset {
      border: 2px solid #666;
      padding: 20px;
      margin-bottom: 20px;
    }

    input, select {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      box-sizing: border-box;
    }

    .form-group {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
    }

    .form-group > div {
      flex: 1 1 200px;
    }

    audio, video {
      width: 100%;
      max-width: 300px;
      display: block;
      margin-bottom: 20px;
    }

    @media (min-width: 768px) {
      .form-group {
        flex-direction: row;
      }
    }

    @media (min-width: 1024px) {
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 40px;
      }

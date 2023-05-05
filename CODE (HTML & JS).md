# WEB-Assignment
CODE IN HTML AND JSS 
<!DOCTYPE html>
<html>
<head>
  <title>Timer Example</title>
</head>
<body>
  <h1>Timer Example</h1>

  <label for="hours-input">Hours:</label>
  <input type="number" id="hours-input" min="0">
  <label for="minutes-input">Minutes:</label>
  <input type="number" id="minutes-input" min="0" max="59">
  <label for="seconds-input">Seconds:</label>
  <input type="number" id="seconds-input" min="0" max="59">

  <button id="start-button">Start Timer</button>

  <script>
    // Get references to the input fields and button
    const hoursInput = document.getElementById('hours-input');
    const minutesInput = document.getElementById('minutes-input');
    const secondsInput = document.getElementById('seconds-input');
    const startButton = document.getElementById('start-button');

    // Get reference to the audio element for the alert sound
    const alertSound = new Audio('path/to/alert/sound.mp3');

    let timerId; // This variable will hold the ID of the timer, so we can cancel it if needed

    // Function to start the timer
    function startTimer() {
      // Get the input values and convert to seconds
      const hours = parseInt(hoursInput.value) || 0;
      const minutes = parseInt(minutesInput.value) || 0;
      const seconds = parseInt(secondsInput.value) || 0;
      const totalSeconds = hours * 3600 + minutes * 60 + seconds;

      // Start the timer
      timerId = setTimeout(() => {
        // Play the alert sound and show the window alert
        alertSound.play();
        window.alert('Timer expired!');

        // Reset the input fields
        hoursInput.value = '';
        minutesInput.value = '';
        secondsInput.value = '';
      }, totalSeconds * 1000);
    }

    // Add click event listener to the start button
    startButton.addEventListener('click', startTimer);
  </script>
</body>
</html>

CODE ONLY FOR JSCRIPT
// Get references to the input fields and button
const hoursInput = document.getElementById('hours-input');
const minutesInput = document.getElementById('minutes-input');
const secondsInput = document.getElementById('seconds-input');
const startButton = document.getElementById('start-button');

// Get reference to the audio element for the alert sound
const alertSound = new Audio('path/to/alert/sound.mp3');

let timerId; // This variable will hold the ID of the timer, so we can cancel it if needed

// Function to start the timer
function startTimer() {
  // Get the input values and convert to seconds
  const hours = parseInt(hoursInput.value) || 0;
  const minutes = parseInt(minutesInput.value) || 0;
  const seconds = parseInt(secondsInput.value) || 0;
  const totalSeconds = hours * 3600 + minutes * 60 + seconds;

  // Start the timer
  timerId = setTimeout(() => {
    // Play the alert sound and show the window alert
    alertSound.play();
    window.alert('Timer expired!');

    // Reset the input fields
    hoursInput.value = '';
    minutesInput.value = '';
    secondsInput.value = '';
  }, totalSeconds * 1000);
}

// Add click event listener to the start button
startButton.addEventListener('click', startTimer);

<script>
    let showPopup = false; // Reactive state to track popup visibility
  
    function togglePopup() {
      showPopup = !showPopup; // Toggle the popup visibility
    }
  
    function callPolice() {
      console.log("Calling the police...");
      showPopup = false; // Close the popup after confirmation
    }
  </script>
  
  <!-- Emergency Circular Button -->
  <div class="emergency-button" on:click={togglePopup}>
    <img src="/emergency-icon.png" alt="Emergency Icon" />
  </div>
  
  <!-- Popup -->
  {#if showPopup}
    <div class="popup-overlay">
      <div class="popup-content">
        <button class="back-button" on:click={togglePopup}>⬅</button>
        <h2>Do you want to call the police?</h2>
        <img class="popup-icon" src="/emergency-icon.png" alt="Emergency Icon" />
        <div class="popup-actions">
          <button class="confirm-button" on:click={callPolice}>YES</button>
          <button class="close-button" on:click={togglePopup}>NO</button>
        </div>
      </div>
    </div>
  {/if}
  
  <style>
    /* Circular Emergency Button Styling */
    .emergency-button {
      position: absolute;
      top: 20px;
      right: 20px;
      width: 120px;
      height: 120px;
      background-color: rgba(111, 111, 112, 0.8);
      border-radius: 50%;
      box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.3);
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      z-index: 10;
    }
  
    .emergency-button img {
      width: 70px;
      height: 70px;
    }
  
    .emergency-button:hover {
      background-color: rgba(111, 111, 112, 1);
      transition: background-color 0.3s ease;
    }
  
    /* Popup Overlay Styling */
    .popup-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5); /* Dim background */
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 20;
    }
  
    /* Larger Popup Content Styling */
    .popup-content {
      position: relative;
      background: rgba(131, 1, 1, 0.85); /* Slightly transparent red background */
      color: white;
      text-align: center;
      padding: 50px;
      border-radius: 16px;
      width: 90%; /* Adjust for responsiveness */
      max-width: 800px; /* Larger max size for bigger screens */
      box-shadow: 0px 6px 8px rgba(0, 0, 0, 0.3); /* Subtle shadow for depth */
    }
  
    .popup-content h2 {
      font-size: 40px; /* Larger font size */
      font-weight: bold;
      margin-bottom: 30px;
    }
  
    .popup-icon {
      width: 120px; /* Larger icon size */
      height: 120px;
      margin: 30px 0;
    }
  
    /* Back Button */
    .back-button {
      position: absolute;
      top: 20px;
      left: 20px;
      background: transparent;
      color: white;
      font-size: 40px; /* Larger arrow size */
      padding: 10px; /* Add padding for a larger clickable area */
      border: none;
      cursor: pointer;
    }
  
    .back-button:hover {
      color: #ccc; /* Light gray on hover */
      transition: color 0.2s ease; /* Smooth transition */
    }
  
    /* Popup Buttons */
    .popup-actions {
      display: flex;
      justify-content: space-around;
      margin-top: 40px;
    }
  
    .confirm-button,
    .close-button {
      width: 200px; /* Wider buttons */
      height: 70px; /* Taller buttons */
      background: rgba(0, 0, 0, 0.8);
      color: white;
      font-size: 24px; /* Larger text */
      font-weight: bold;
      border: none;
      border-radius: 16px; /* More rounded corners */
      cursor: pointer;
    }
  
    .confirm-button:hover {
      background: rgba(0, 128, 0, 0.8); /* Green hover effect for YES */
    }
  
    .close-button:hover {
      background: rgba(128, 0, 0, 0.8); /* Dark red hover effect for NO */
    }
  </style>
  
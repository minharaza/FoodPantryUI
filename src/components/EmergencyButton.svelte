<script>
    let showPopup = false; // Reactive state to track popup visibility
  
    function togglePopup() {
      showPopup = !showPopup; // Toggle the popup visibility
      console.log("Popup state:", showPopup); // Debug: Check state changes
    }
  </script>
  
  <!-- Emergency Circular Button -->
  <div class="emergency-button" on:click={togglePopup}>
    <img src="/emergency-icon.png" alt="Emergency Icon" />
  </div>
  
  <!-- Popup -->
  {#if showPopup}
    <div class="popup-overlay" on:click={togglePopup}>
      <div class="popup-content" on:click|stopPropagation>
        <h2>Emergency Alert</h2>
        <p>Are you sure you want to trigger the emergency?</p>
        <div class="popup-actions">
          <button on:click={togglePopup} class="close-button">Cancel</button>
          <button class="confirm-button">Confirm</button>
        </div>
      </div>
    </div>
  {/if}
  
  <style>
    /* Larger Circular Emergency Button Styling */
    .emergency-button {
      position: absolute; /* For placement */
      top: 20px; /* Adjust for layout */
      right: 20px; /* Adjust for layout */
      width: 120px; /* Increased size */
      height: 120px; /* Circle size (same as width) */
      background-color: rgba(111, 111, 112, 0.8); /* Add transparency with rgba */
      border-radius: 50%; /* Makes the button circular */
      box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.3); /* Subtle shadow */
      display: flex; /* Center the icon */
      justify-content: center; /* Center horizontally */
      align-items: center; /* Center vertically */
      cursor: pointer; /* Pointer cursor */
      z-index: 10; /* Ensure it's above other elements */
    }
  
    .emergency-button img {
      width: 60px; /* Adjusted icon size for the larger button */
      height: 60px; /* Keep icon proportional */
      opacity: 0.9; /* Slight transparency for the icon */
    }
  
    .emergency-button:hover {
      background-color: rgba(111, 111, 112, 1); /* Remove transparency on hover */
      transition: background-color 0.3s ease; /* Smooth hover transition */
    }
  
    /* Popup Overlay Styling */
    .popup-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5); /* Semi-transparent black */
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 20; /* Ensure it's above the button */
    }
  
    /* Popup Content Styling */
    .popup-content {
      background: white;
      padding: 20px;
      border-radius: 8px;
      text-align: center;
      width: 300px;
      box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.3);
    }
  
    .popup-content h2 {
      margin-top: 0;
      font-size: 20px;
      color: #e63946;
    }
  
    .popup-content p {
      margin: 10px 0;
      font-size: 14px;
    }
  
    /* Popup Buttons */
    .popup-actions {
      margin-top: 15px;
      display: flex;
      justify-content: space-between;
    }
  
    .close-button {
      background: gray;
      color: white;
      border: none;
      border-radius: 5px;
      padding: 8px 12px;
      cursor: pointer;
    }
  
    .close-button:hover {
      background: darkgray;
    }
  
    .confirm-button {
      background: #e63946;
      color: white;
      border: none;
      border-radius: 5px;
      padding: 8px 12px;
      cursor: pointer;
    }
  
    .confirm-button:hover {
      background: #b71c1c;
    }
  </style>
  
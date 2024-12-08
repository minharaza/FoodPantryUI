<script>
    export let icon = '/emergency-icon.png'; // Relative path from the `static` folder
  </script>
  
  <div class="emergency-button">
    <img src={icon} alt="Emergency Icon" />
  </div>
  
  <style>
    .emergency-button {
      position: absolute;
      top: 20px;
      right: 20px;
      background: #6F6F70;
      padding: 10px;
      border-radius: 50%;
    }
    .emergency-button img {
      width: 40px;
      height: 40px;
    }
  </style>
  
<script>
    export let icon = '/path-to-emergency-icon.png';
  </script>
  
  <div class="emergency-button">
    <img src={icon} alt="Emergency Icon" />
  </div>
  
  <style>
    .emergency-button {
      position: absolute;
      top: 20px;
      right: 20px;
      background: red;
      padding: 10px;
      border-radius: 50%;
    }
    .emergency-button img {
      width: 40px;
      height: 40px;
    }
  </style>
  
<script>
    export let icon;
    export let alt = 'button icon';
  </script>
  
  <div class="icon-button">
    <img src={icon} alt={alt} />
  </div>
  
  <style>
    .icon-button {
      background: #4c4c4c;
      border-radius: 10px;
      padding: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .icon-button img {
      width: 40px;
      height: 40px;
    }
  </style>
  
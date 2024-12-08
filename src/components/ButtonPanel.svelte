<script>
    import IconButton from './IconButton.svelte';
  </script>
  
  <div class="button-panel">
    <IconButton icon="/path-to-star-icon.png" alt="Star Icon" />
    <IconButton icon="/path-to-map-pin-icon.png" alt="Map Pin Icon" />
    <IconButton icon="/path-to-phone-icon.png" alt="Phone Icon" />
    <IconButton icon="/path-to-safe-place-icon.png" alt="Safe Place Icon" />
  </div>
  
  <style>
    .button-panel {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
  </style>
  
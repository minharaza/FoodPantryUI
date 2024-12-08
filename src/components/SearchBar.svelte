<script>
    export let placeholder = 'Search something';
  </script>
  
  <div class="search-bar">
    <input type="text" placeholder={placeholder} />
  </div>
  
  <style>
    .search-bar input {
      padding: 0.5rem;
      border-radius: 10px;
      border: none;
      width: 100%;
      max-width: 300px;
    }
  </style>
  
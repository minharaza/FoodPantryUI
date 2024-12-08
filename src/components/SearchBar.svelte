<script>
  export let placeholder = "Search something"; // Placeholder for the search bar
</script>

<div class="search-bar">
  <img src="/search-icon.png" alt="Search Icon" class="search-icon" />
  <input type="text" placeholder={placeholder} />
</div>

<style>
  /* Search Bar Container */
  .search-bar {
    position: absolute; /* Position relative to parent container */
    top: 20px; /* Distance from the top */
    left: 20px; /* Distance from the left edge */
    width: 300px; /* Fixed width for the search bar */
    height: 50px; /* Height of the search bar */
    background-color: rgba(94, 43, 43, 0.655); /* Semi-transparent red background */
    border-radius: 25px; /* Rounded corners */
    display: flex; /* Flex container for alignment */
    align-items: center; /* Center content vertically */
    padding: 0 15px; /* Padding for inner content */
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2); /* Subtle shadow for depth */
    z-index: 10; /* Ensure it's above other elements */
  }

  /* Search Icon Styling */
  .search-icon {
    width: 24px; /* Icon width */
    height: 24px; /* Icon height */
    margin-right: 10px; /* Space between icon and input field */
  }

  /* Search Input Field */
  .search-bar input {
    width: 100%; /* Take full width of the container */
    height: 100%; /* Match container height */
    background: transparent; /* Transparent background */
    border: none; /* Remove default border */
    outline: none; /* Remove focus outline */
    color: white; /* Text color */
    font-size: 16px; /* Font size */
    font-weight: 500; /* Slightly bolder text */
  }

  /* Placeholder Text */
  .search-bar input::placeholder {
    color: rgba(255, 255, 255, 0.7); /* Semi-transparent white */
    font-style: italic; /* Italicized placeholder */
  }
</style>

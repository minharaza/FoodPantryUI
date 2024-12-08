<script>
    import ButtonPanel from "../components/ButtonPanel.svelte";
    import CurrentLocation from "../components/CurrentLocation.svelte";
    import EmergencyButton from "../components/EmergencyButton.svelte";
    import Map from "../components/Map.svelte";
    import SearchBar from "../components/SearchBar.svelte";
  </script>
  
  <div class="map-page">
    <div class="map-background">
      <SearchBar placeholder="Search something" />
      <ButtonPanel />
      <Map />
      <EmergencyButton />
      <CurrentLocation location="Clifton — Cincinnati" />
    </div>
  </div>
  
  <style>
    .map-page {
      position: relative;
      width: 100%;
      height: 100vh;
      background: #000;
      color: #fff;
    }
  
    .map-background {
      background-image: url('/map-background.png');
      background-size: cover;
      background-position: center;
      height: 100%;
      width: 100%;
    }
  </style>
  
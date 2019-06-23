<script>
  import Cloud from "./Cloud.svelte";

  export let name;
</script>

<style>
  .element {
    margin: auto;
    position: absolute;
    height: 250px;
    width: 250px;
    /* animation: pulse 5s ease infinite alternate; */
    background-color: gold;
    border: 0;
    border-radius: 100%;
    box-shadow: 0px 0px 60px 10px #fbe602, 0 0 100px 60px #e70f14,
      0 0 200px 190px #fabc14;
  }

  @keyframes pulse {
    0% {
      background-color: yellow;
    }
    50% {
      background-color: orange;
    }
    100% {
      background-color: darkorange;
    }
  }

  @keyframes nudge {
    0% {
      transform: translate(0, 0);
    }
    100% {
      transform: translate(200px, 0);
    }

    50% {
      transform: translate(80px, 0);
    }

    80% {
      transform: translate(150px, 0);
    }
  }
  @keyframes grow {
    0% {
      transform: scale(0.3);
    }
    100% {
      transform: scale(1);
    }

    50% {
      transform: scale(0.5);
    }

    80% {
      transform: scale(0.7);
    }
  }
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    background-color: lightskyblue;
  }
  h1 {
    user-select: none;
    -moz-user-select: none;
  }
  .cloud-container {
    width: 100%;
    height: 100%;
    background: linear-gradient(0deg, #62a0d8 0%, #2178d1 50%, #085cb3 100%);
    overflow: hidden;
  }
</style>

<!-- <div class="container"> -->
<!-- -->
<!-- <h1>{name}</h1> -->
<!-- </div> -->

<!-- <div class="element" /> -->
<div class="cloud-container">
  <Cloud left="300px" top="200px" seed="11112" filterId="a"/>
  <Cloud  left="0px" top="0px" seed="11" filterId="b"/>
  <Cloud  left="-200px" top="150px" seed="333" filterId="c"/>
</div>

<script>
  export let name;
</script>

<style>
  .element {
    position: absolute;
    opacity: 0.5;
    height: 350px;
    width: 350px;
    background-color: red;
    animation: pulse 2s ease infinite alternate,
      grow 2s linear infinite alternate;
    border-radius: 100%;
    box-shadow: 0 0 60px 30px #fbe602, 0 0 100px 60px #e70f14,
      0 0 140px 90px #fabc14;
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
    0%,
    100% {
      transform: translate(0, 0);
    }

    50% {
      transform: translate(150px, 0);
    }

    80% {
      transform: translate(-150px, 0);
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
  .sky {
    position: absolute;
    width: 100vw;
    height: 100vh;
  }
</style>

<div class="container">
  <h1>{name}</h1>
  <div class="element" />
</div>

<template>
  <div class="app">
    <h1>Hello!</h1>
    <Tweet name='Thoughts of Dog®' image='https://i.imgur.com/b0EdHVV.jpg'  handle='dog_feelings' timestamp='1h ago'
    message='the human likes to say. that i live here rent free. but i would argue.
  this housing accommodation.
  is my payment. for a lifetime of love. and excellent company'/>
  </div>
</template>

<script>
import Tweet from './components/Tweet.vue';

export default {
  name: 'App',
  components: { Tweet },
};
</script>

<style>
  body {
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
      "Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
      sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  .app {
    text-align: center;
  }

  .app-logo {
    height: 40vmin;
    pointer-events: none;
  }

  @media (prefers-reduced-motion: no-preference) {
    .app-logo {
      animation: App-logo-spin infinite 20s linear;
    }
  }

  .app-header {
    background-color: #282c34;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: calc(10px + 2vmin);
    color: white;
  }

  .app-link {
    color: #61dafb;
  }

  @keyframes App-logo-spin {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }

  .app {
    padding: 20px;
  }
</style>

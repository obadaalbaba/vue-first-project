<template>
  <section>
    <header>
      <h1>My Friends</h1>
      <button v-on:click="changeVisibility">Show/Hide Details</button>
    </header>
    <ul v-if=areFriendsVisible>
      <li>
        <h2>{{ friends[0].name }}</h2>
        <button>
          Show Details
        </button>
        <ul>
          <li>
            <strong>Phone:</strong>
            {{ friends[0].phone }}
          </li>
          <li>
            <strong>Email:</strong>
            {{ friends[0].email }}
          </li>
        </ul>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
        areFriendsVisible: false,
        friends: [
          {
            name: 'Obada',
            phone: '514-123-4567',
            email: 'obadaalbaba94@gmail.com'
          }
        ]
    }
  },
  methods: {
    changeVisibility() {
      this.areFriendsVisible = !this.areFriendsVisible
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  font-family: "Jost", sans-serif;
}
body {
  margin: 0;
}
header {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem auto;
  border-radius: 10px;
  padding: 1rem;
  background-color: #58004d;
  color: white;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
li {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}
h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #58004d;
  margin: 0 0 1rem 0;
}
button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}
button:hover,
button:active {
  background-color: #ec3169;
  border-color: #ec3169;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}
</style>

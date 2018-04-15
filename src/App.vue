<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Accordion title="Press me to roll down" id="1">
      <h3>Something fun!</h3>
      <p>Hi all, something fun is up tonight!</p>
    </Accordion>
    <Accordion title="Til I collapse" id="2">
      <h3>Something even funnier!</h3>
      <p>'Cause sometimes you just feel tired, you feel weak
And when you feel weak you feel like you want to just give up
But you gotta search within you, you gotta find that inner strength
And just pull that shit out of you and get that motivation to not give up
And not be a quitter, no matter how bad you want to just fall flat on your face and collapse
'Til I collapse I'm spilling these raps long as you feel 'em
'Til the day that I drop you'll never say that I'm not killing 'em
'Cause when I am not then I'm a stop pinning them
And I am not hip-hop and I'm just not Eminem
Subliminal thoughts when I'm stop sending them
Women are caught in webs spin and hock venom
Adrenaline shots of penicillin could not get the illin' to stop
Amoxicillin is just not real enough
The criminal cop killing hip-hop filling a
Minimal swap to cop millions of Pac listeners
You're coming with me, feel it or not
You're gonna fear it like I showed you the spirit of god lives in us
You hear it a lot, lyrics that shock, is it a miracle
Or am I just a product of pop fizzing up
For shizzle my whizzle this is the plot listen up
You Bizzles forgot Slizzle does not give a fuck</p>
    </Accordion>
  </div>
</template>

<script>
import Accordion from "./components/Accordion.vue";

export default {
  name: "app",
  components: {
    Accordion
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<template>
  <div class="container">
    <div class="contents">
      <img :src="illustrationHero" alt="music-image" />
      <h1>Order Summary</h1>
      <p>
        You can now listen to millions of songs, audiobooks, and podcasts on any
        device anywhere you like!
      </p>
      <div class="details">
        <img :src="iconMusic" alt="music-logo" />
        <div id="price">
          <h3>Annual Plan</h3>
          <p>$59.99/year</p>
        </div>
        <a id="change" href="#" @click="changePlan">Change</a>
      </div>
      <div class="btn">
        <button id="proceed" type="submit" @click="SubmitForm()">
          Proceed to Payment
        </button>
        <h3 id="cancel" @click="cancelOrder"><a href="#">Cancel order</a></h3>
      </div>
    </div>
  </div>
</template>
<script>
import illustrationHeroPic from "../assets/illustration-hero.svg";
import icon from "../assets/icon-music.svg";
export default {
  data() {
    return {
      illustrationHero: illustrationHeroPic,
      iconMusic: icon,
    };
  },
  methods: {
    SubmitForm() {
      alert("Payment made sucessfully");
      location.reload();
    },
    cancelOrder() {
      alert("Payment cancelled");
    },
    changePlan(){
      alert("Plan changed");
    }
  },
};
</script>

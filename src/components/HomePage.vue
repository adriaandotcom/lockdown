<template>
  <div>
    <Map></Map>
    <div class="legend">
      <ul>
        <li class="yes">Lockdown</li>
        <li class="mild">Milde lockdown</li>
        <li class="no">Geen lockdown</li>
        <li class="unkown">Niet bekend</li>
        <li class="no-eu">Buiten EU</li>
      </ul>
    </div>
    <div class="link">
      <a :href="doc" target="_blank">Bewerk gegevens</a>
      <p>
        Gemaakt door
        <a href="https://www.instagram.com/swissjurriens/">Swiss</a> &
        <a href="https://twitter.com/AdriaanvRossum" target="_blank">Adriaan</a>
      </p>
    </div>
  </div>
</template>

<script>
import Map from "./Map.vue";
import { doc } from "../config/constants";

export default {
  name: "HomePage",

  data() {
    return {
      doc
    };
  },

  components: {
    Map
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.legend {
  position: absolute;
  bottom: 1.7rem;
  left: 1.7rem;
}
.link {
  position: absolute;
  bottom: 1.3rem;
  right: 1.7rem;
}
.link > a {
  background-color: white;
  border-radius: 5px;
  box-shadow: 1px 1px 5px grey;
  display: block;
  padding: 0.5rem 1rem;
  color: #1c4587;
}
.link p {
  font-size: 11px;
  text-align: right;
  margin: 0.5rem 0 0 0;
}
a {
  color: #1c4587;
  text-decoration: none;
}
ul {
  padding: 0;
  margin: 0;
  list-style-type: none;
}
ul li::before {
  content: "";
  display: inline-block;
  margin-right: 0.5rem;
  width: 10px;
  height: 10px;
  border-radius: 10px;
}
ul li.yes::before {
  background-color: #1c4587;
}
ul li.mild::before {
  background-color: #e98980;
}
ul li.no::before {
  background-color: #ea4335;
}
ul li.unkown::before {
  background-color: #d9d9d9;
}
ul li.no-eu::before {
  background-color: #c0c0c0;
}
</style>

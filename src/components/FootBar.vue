<template>
  <footer class="footer">
    <h3 class="centretext">We operate in many other cities.</h3>
    <div id="citylist">
      <div class="country">
        <h3>India</h3>
        <ul>
          <li>Bangalore</li>
          <li>Hyderabad</li>
          <li>Delhi</li>
          <li>Lucknow</li>
          <li>Jaipur</li>
          <li>Jodhpur</li>
        </ul>
      </div>
      <div class="country">
        <h3>India</h3>
        <ul>
          <li>Bangalore</li>
          <li>Hyderabad</li>
          <li>Delhi</li>
          <li>Lucknow</li>
          <li>Jaipur</li>
          <li>Jodhpur</li>
        </ul>
      </div>
    </div>
    <hr />
    <h3 class="centretext">
      {{
        new Date().getFullYear() -
        1 +
        " - " +
        new Date().getFullYear() +
        " " +
        "Zoomcar Ltd."
      }}
    </h3>
    <h3 class="centretext">All Right Reserved</h3>
  </footer>
</template>


<script>
export default {
  name: "FootBar",
};
</script>

<style>
.footer {
  padding-top: 1%;
  padding-bottom: 1%;
  background-color: darkgray;
  color: white;
  margin: 0% auto 1% auto;
  width: 40%;
  height: 30%;
}
.centretext {
  padding: 1%;
  text-align: center;
}
.country {
  display: inline-block;
  margin: 5%;
  list-style-type: none;
  text-align: center;
}
ul {
  list-style-type: none;
}
</style>
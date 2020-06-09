<template>
  <div class="homecontainer">
    <div id="main-image">
      <img src="@/assets/koi.jpg" />
    </div>
    <h2 id="header">Welcome to the pond</h2>
    <div id="main-description">
      <p>
        We have some koi in our restaurant.
        Don't spell it coy or they'll get offended
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "About",
  data() {
    return {};
  }
};
</script>

<style>
.homecontainer {
  display: grid;
  width: 50%;
  grid-template-columns: 1fr 1fr 1.5fr;
  grid-template-areas:
    "main main header"
    "main main description"
    "main main description"
    "footer footer footer";
  margin: 0px 0px;
  padding-left: 15px;
}

#main-image {
  grid-area: main;
  padding-top: 15px;
}

#main-image img {
  width: 100%;
}

#main-description {
  grid-area: description;
  padding-left: 15px;
  align-items: end;
}

#header {
  grid-area: header;
  padding-left: 15px;
  align-self: end;
}
</style>

<template>
  <div>
    <h2>Our pond is full of food</h2>
    <div v-for="(item, index) in menuItems" :key="index">
      <h3>{{`${index+1}. ${item.title}`}}</h3>
      <p>{{item.description}}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "Menu",
  data() {
    return {
      menuItems: [
        {
          title: "sushi",
          description: "we got sushi, dog"
        },
        {
          title: "burrito",
          description:
            "we're making uh... we're makin burritos out..um...out here in this place"
        },
        {
          title: "fish",
          description: "fish! you kiddin? yeah I think we have some"
        },
        {
          title: "veggies",
          description: "let me tell you bout these hills up in these mountains"
        },
        {
          title: "napkins",
          description: "stay fresh"
        }
      ]
    };
  }
};
</script>
<template>
  <div>
    <div>
      <h1>Your Tweets</h1>
    </div>
    <div id="tweet-container">
      <div v-for="tweet in tweets" :key="tweet">
        <p>{{tweet.tweet}}</p>
        <h2>{{tweet.Name}}</h2>
        <h2>{{tweet.date}}</h2>
      </div>
       
       <button v-if="gridStyle" @click="gridStyle=!true">Switch to list</button>
       <button v-else>Switch to grid</button>
      <div v-bind:class="{gridStyle: isGrid, list: isList}"></div>

    </div>
  </div>
</template>

<script>
export default {
  name: "page-body",
  data: function () {
    return {
      tweets: [
        { tweet: "Hello", Name: "Bill", date: "08-01-2020" },
        { tweet: "Hey", Name: "Bob", date: "09-01-2020" },
        { tweet: "Greetings", Name: "Bonnie", date: "09-01-2019" },
        { tweet: "Yo", Name: "Robert", date: "09-01-2020" },
      ],
    };
  },
};
</script>

<style lang="stylus" scoped></style>


<style scoped>
* {
  padding: 0;
  margin: 0;
}
.page-body {
  display: grid;
  justify-items: center;
  align-items: center;
  grid-template-columns: (1fr, 1fr, 1fr, 1fr);
  grid-template-rows: minmax();
  width: 100%;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
#container-grid {
  display: grid;
}


</style>
  



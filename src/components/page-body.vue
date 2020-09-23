<template>
  <div>
    <div>
      <h1>Your Tweets</h1>
    </div>
    <div id="tweet-container" v-bind:class="{pagegrid: grid}">
      <div v-for="tweet in tweets" :key="tweet.tweet">
        <p>{{tweet.tweet}}</p>
        <h2>{{tweet.Name}}</h2>
        <h2>{{tweet.date}}</h2>
      </div>
       
   
      

    </div>
        <button v-if="grid" @click="grid=!grid">Switch to list</button>
       <button v-else @click="grid=!grid">Switch to grid</button>
  </div>
</template>

<script>
export default {
  name: "page-body",
  data: function () {
    return {
      grid: false,
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
.pagegrid {
  display: grid;
  grid-template-columns: repeat(5, 1fr)
}

</style>
  



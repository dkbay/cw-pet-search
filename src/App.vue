<template>
  <div id="app">
    <img class="logo" alt="Cube World Logo" src="https://cubeworld.com/media/cube-world-logo.png" />
    <div class="container">
      <div class="search">
        <h1>Cube World pet food helper</h1>
        <p>
          Find out what pet food you need or what pet you can tame with your
          food
        </p>
        <VueFuse placeholder="Pet or Food Name" event-name="results" :list="petData" :keys="keys" :threshold="0.3" />
      </div>
      <div class="results">
        <div v-for="result in results" :key="result.food" class="result">
          <div class="result-image">
            <img :src="'/img/' + result.food + '.png'" alt="" />
          </div>
          <div class="result-info">
            <div class="result-text">
              <h3>{{ result.food }}</h3>
              <p>{{ result.name }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      results: [],
      keys: ["name", "food"],
      petData: [
        {
          name: "Crocodile",
          food: "Apple Ring",
        },

        {
          name: "Monkey",
          food: "Banana Split",
        },

        {
          name: "Bumblebee",
          food: "Biscuit Roll",
        },

        {
          name: "Porcupine",
          food: "Blackberry Marmalade",
        },

        {
          name: "Mosquito",
          food: "Bloodorange Juice",
        },

        {
          name: "Beaver",
          food: "Buckhorn",
        },

        {
          name: "Collie",
          food: "Bubble Gum",
        },

        {
          name: "Blue Slime",
          food: "Blue Jelly",
        },

        {
          name: "Bark Beetle",
          food: "Bread",
        },

        {
          name: "Snail",
          food: "Cabbage rolls",
        },

        {
          name: "Horse",
          food: "Candied Apple",
        },

        {
          name: "Cat (Only Black)",
          food: "Candy",
        },

        {
          name: "Desert runner",
          food: "Caramel Chocolate Bar",
        },

        {
          name: "Bunny",
          food: "Carrot",
        },

        {
          name: "Chicken",
          food: "Cereal Bar",
        },

        {
          name: "Turtle",
          food: "Cinnamon Roll",
        },

        {
          name: "Raccoon",
          food: "Chocolate Cake",
        },

        {
          name: "Peacock",
          food: "Chocolate Cookie",
        },

        {
          name: "Brown Alpaca",
          food: "Chocolate Cupcake",
        },

        {
          name: "Mole",
          food: "Chocolate Donut",
        },

        {
          name: "Baby Mammoth",
          food: "Chocolate Ice Cream",
        },

        {
          name: "Sheep",
          food: "Cotton Candy",
        },

        {
          name: "Scottish Terrier",
          food: "Croissant",
        },

        {
          name: "Fire Beetle",
          food: "Curry",
        },

        {
          name: "Camel",
          food: "Date Cookie",
        },

        {
          name: "Koala",
          food: "Eucalyptus Candy",
        },

        {
          name: "Fly",
          food: "Fruit Basket",
        },

        {
          name: "Parrot",
          food: "Ginger Tartlet",
        },

        {
          name: "Green Slime",
          food: "Green Jelly",
        },

        {
          name: "Lemon Beetle",
          food: "Lemon Tart",
        },

        {
          name: "Crow",
          food: "Licorice Candy",
        },

        {
          name: "Owl",
          food: "Lollipop",
        },

        {
          name: "Snout Beetle",
          food: "Lolly",
        },

        {
          name: "Bat",
          food: "Mango Juice",
        },

        {
          name: "Midge",
          food: "Melon Ice Cream",
        },

        {
          name: "Radishling Sprout",
          food: "Mineral Water",
        },

        {
          name: "Leaf Runner",
          food: "Mint Chocolate Bar",
        },

        {
          name: "Caterpillar",
          food: "Mixed Salad",
        },

        {
          name: "Biter",
          food: "Pancakes",
        },

        {
          name: "Baby Elephant",
          food: "Peanut",
        },

        {
          name: "Pink Slime",
          food: "Pink Jelly",
        },

        {
          name: "Hornet",
          food: "Popcorn",
        },

        {
          name: "Pig",
          food: "Pumpkin Mash",
        },

        {
          name: "Earth Caterpillar",
          food: "Radicchio Salad",
        },

        {
          name: "Flamingo",
          food: "Raspberry Juice",
        },

        {
          name: "Plain Runner",
          food: "Rice Milk Chocolate Bar",
        },

        {
          name: "Seagull",
          food: "Salted Caramel",
        },

        {
          name: "Penguin",
          food: "Soft Ice",
        },

        {
          name: "Cornling Sprout",
          food: "Spring Water",
        },

        {
          name: "Squirrel",
          food: "Strawberry Cake",
        },

        {
          name: "Crab",
          food: "Strawberry Cocktail",
        },

        {
          name: "Duckbill",
          food: "Sugar Candy",
        },

        {
          name: "Alpaca (Light)",
          food: "Vanilla Cupcake",
        },

        {
          name: "Terrier",
          food: "Waffle",
        },

        {
          name: "Spitter",
          food: "Water Ice",
        },

        {
          name: "Snow Runner",
          food: "White Chocolate Bar",
        },

        {
          name: "Yellow Slime",
          food: "Yellow Jelly",
        },
      ],
    };
  },
  created() {
    this.$on("results", (results) => {
      this.results = results;
    });
  },
};
</script>

<style>
html,
body {
  margin: 0;
}

#app {
  font-family: "Raleway", sans-serif;
  background-color: #173627;
  min-height: 100vh;
  padding-bottom: 100px;
}

.logo {
  display: block;
  margin: 0 auto;
  width: 400px;
  max-width: 80%;
  padding-top: 50px;
}

.container {
  display: grid;
  justify-content: center;
}

.search {
  color: #fefefe;
  text-align: center;
}

input {
  background-color: #d3e7dd;
  outline: none;
  border: none;
  padding: 10px;
  border-radius: 3px;
  width: 100%;
  color: #333;
  font-size: 18px;
  box-sizing: border-box;
}

.results {
  margin-top: 25px;
  display: grid;
  grid-template-rows: 1fr;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  min-width: 650px;
}

.result {
  display: grid;
  grid-template-columns: 25% 75%;
  background-color: #09241b;
  color: rgb(211, 231, 221);
  padding: 16px;
  border-radius: 8px;
  box-shadow: rgb(76 76 76 / 10%) 4px 4px 8px 0px;
}

.result-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.result-image>img {
  width: 100%;
  max-width: 45px;
}

.result-text {
  padding-left: 10px;
}
</style>

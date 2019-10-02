<template>
  <div class="container" searchcomponent>
    <div class="search">
      <h1>Cube World pet food helper</h1>
      <p>Find out what pet food you need or what pet you can tame with your food</p>
      <VueFuse 
        placeholder="Pet or Food Name"
        event-name="results"
        :list="petData"
        :keys="keys"
      />
    </div>
    <div class="results">
      <div v-for="result in results" :key="result.food" class="result">
        <div class="result-image">
          <img src="https://gamepedia.cursecdn.com/cube_gamepedia/thumb/4/4f/Apple_Ring.png/45px-Apple_Ring.png?version=2c115c190785855ffb9b81161d6644f4" alt="">
        </div>
        <div class="result-info">
          <h3>{{ item.food }}</h3>
          <p>{{ item.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Search',
  data () {
    return {
      results: [],
      keys: ["name", "food"],
      petData: 
      [
        {
            "name":"Crocodile",
            "food":"Apple Ring"
        },

        {
            "name":"Monkey",
            "food":"Banana Split"
        },

        {
            "name":"Bumblebee",
            "food":"Biscuit Roll"
        },

        {
            "name":"Porcupine",
            "food":"Blackberry Marmalade"
        },

        {
            "name":"Mosquito",
            "food":"Bloodorange Juice"
        },

        {
            "name":"Beaver",
            "food":"Buckhorn"
        },

        {
            "name":"Collie",
            "food":"Bubble Gum"
        },

        {
            "name":"Blue Slime",
            "food":"Blue Jelly"
        },

        {
            "name":"Bark Beetle",
            "food":"Bread"
        },

        {
            "name":"Snail",
            "food":"Cabbage rolls"
        },

        {
            "name":"Horse",
            "food":"Candied Apple"
        },

        {
            "name":"Cat (Only Black)",
            "food":"Candy"
        },

        {
            "name":"Desert runner",
            "food":"Caramel Chocolate Bar"
        },

        {
            "name":"Bunny",
            "food":"Carrot"
        },

        {
            "name":"Chicken",
            "food":"Cereal Bar"
        },

        {
            "name":"Turtle",
            "food":"Cinnamon Roll"
        },

        {
            "name":"Raccoon",
            "food":"Chocolate Cake"
        },

        {
            "name":"Peacock",
            "food":"Chocolate Cookie"
        },

        {
            "name":"Brown Alpaca",
            "food":"Chocolate Cupcake"
        },

        {
            "name":"Mole",
            "food":"Chocolate Donut"
        },

        {
            "name":"Baby Mammoth",
            "food":"Chocolate Ice Cream"
        },

        {
            "name":"Sheep",
            "food":"Cotton Candy"
        },

        {
            "name":"Scottish Terrier",
            "food":"Croissant"
        },

        {
            "name":"Fire Beetle",
            "food":"Curry"
        },

        {
            "name":"Camel",
            "food":"Date Cookie"
        },

        {
            "name":"Koala",
            "food":"Eucalyptus Candy"
        },

        {
            "name":"Fly",
            "food":"Fruit Basket"
        },

        {
            "name":"Parrot",
            "food":"Ginger Tartlet"
        },

        {
            "name":"Green Slime",
            "food":"Green Jelly"
        },

        {
            "name":"Lemon Beetle",
            "food":"Lemon Tart"
        },

        {
            "name":"Crow",
            "food":"Licorice Candy"
        },

        {
            "name":"Owl",
            "food":"Lollipop"
        },

        {
            "name":"Snout Beetle",
            "food":"Lolly"
        },

        {
            "name":"Bat",
            "food":"Mango Juice"
        },

        {
            "name":"Midge",
            "food":"Melon Ice Cream"
        },

        {
            "name":"Radishling Sprout",
            "food":"Mineral Water"
        },

        {
            "name":"Leaf Runner",
            "food":"Mint Chocolate Bar"
        },

        {
            "name":"Caterpillar",
            "food":"Mixed Salad"
        },

        {
            "name":"Biter",
            "food":"Pancakes"
        },

        {
            "name":"Baby Elephant",
            "food":"Peanut"
        },

        {
            "name":"Pink Slime",
            "food":"Pink Jelly"
        },

        {
            "name":"Hornet",
            "food":"Popcorn"
        },

        {
            "name":"Pig",
            "food":"Pumpkin Mash"
        },

        {
            "name":"Earth Caterpillar",
            "food":"Radicchio Salad"
        },

        {
            "name":"Flamingo",
            "food":"Raspberry Juice"
        },

        {
            "name":"Plain Runner",
            "food":"Rice Milk Chocolate Bar"
        },

        {
            "name":"Seagull",
            "food":"Salted Caramel"
        },

        {
            "name":"Penguin",
            "food":"Soft Ice"
        },

        {
            "name":"Cornling Sprout",
            "food":"Spring Water"
        },

        {
            "name":"Squirrel",
            "food":"Strawberry Cake"
        },

        {
            "name":"Crab",
            "food":"Strawberry Cocktail"
        },

        {
            "name":"Duckbill",
            "food":"Sugar Candy"
        },

        {
            "name":"Alpaca (Light)",
            "food":"Vanilla Cupcake"
        },

        {
            "name":"Terrier",
            "food":"Waffle"
        },

        {
            "name":"Spitter",
            "food":"Water Ice"
        },

        {
            "name":"Snow Runner",
            "food":"White Chocolate Bar"
        },

        {
            "name":"Yellow Slime",
            "food":"Yellow Jelly"
        }
    ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container {
    display: grid;
    justify-content: center;
  }
  .search {
  color: #fefefe;
  text-align: center;
  }

  input {
    outline:none;
    border:none;
    padding:10px;
    border-radius: 3px;
    width:100%;
    color:#333;
    font-size: 18px;
    box-sizing: border-box;
  }

  .results {
    margin-top: 25px;
  }

  .result {
    display: grid;
    grid-row-gap: 50px;
    grid-template-columns: 25% 75%;
    background-color: #fefefe;
    padding: 25px;
    border-radius: 3px;
  }

  .result-info {
    padding-left: 25px;
  }

  .result-image {
    display:flex;
    justify-content:center;
    align-items: center;
  }

  .result-image>img {
    width:50%;
  }
</style>

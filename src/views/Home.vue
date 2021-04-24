<template>
  <div class="home">
    <div class="m-4">
      <form action="#" class="space-y-4">
        <div>
          <h1>Product name</h1>
          <input type="text" class="border-2" v-model="prodName" />
        </div>
        <hr />

        <div>
          <h1>Menufacturer Date</h1>
          <label for="birthday">Birthday: &nbsp;</label>
          <input
            class="border-2"
            type="date"
            id="birthday"
            name="birthday"
            v-model="date"
          />
        </div>
        <hr />

        <div class="">
          <h1>Product Description</h1>
          <input class="border-2" type="text" v-model="description" />
        </div>
        <hr />
        <div>
          <h1>Brand</h1>

          <select class="border-2 mb-4" name="" id="" v-model="brand">
            <option value="apple">apple</option>
            <option value="google">google</option>
            <option enable value="samsung">samsung</option>
            <option value="oppo">oppo</option>
          </select>
          <!-- --------v-select------------ -->
          <h1>loop style</h1>
          <select v-model="brandname" class="border-2 mb-2">
            <option
              v-for="brand in brands"
              :key="brand.id"
              :value="brand"
            >
              {{ brand }}
            </option>
          </select>
          <!-- ---------------------- -->

          <div>
            <label for="img">Select image:</label>
            <input type="file" id="img" name="img" accept="image/*" />
          </div>
        </div>

        <div class="space-x-1">
          <h1>Colors</h1>

          <input
            type="checkbox"
            name="red"
            value="red"
            class="bg-red-200"
            v-model="color"
          />
          <label for="red"> red</label><br />
          <input type="checkbox" name="green" value="green" v-model="color" />
          <label for="green"> green</label><br />
          <input type="checkbox" name="blue" value="blue" v-model="color" />
          <label for="blue"> blue</label><br /><br />
        </div>

        <hr />
        <div>
          <h1>Price</h1>
          <input type="text" class="border-2" v-model="price" />
        </div>
        <hr />
        <div class="space-x-2">
          <h1>Warranty</h1>

          <input
            type="radio"
            id="none"
            name="warranty"
            value="none"
            v-model="warranty"
          />
          <label for="none"> none</label><br />
          <input
            type="radio"
            id="oneyear"
            name="warranty"
            value="oneyear"
            v-model="warranty"
          />
          <label for="oneyear">1 year</label><br />
          <input
            type="radio"
            id="threeyear"
            name="warranty"
            value="threeyear"
            v-model="warranty"
          />
          <label for="threeyear">3 year</label>
        </div>

        <input type="submit" class="hover:bg-green-200 p-2" />
      </form>
    </div>

    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Home",
  // components: {
  //   HelloWorld
  // },

  data() {
    return {
      //brands: [{ title: "apple" }, { title: "samsung" }],
      brands:['apple','samsung','oppo']
    };
  },
};
</script>

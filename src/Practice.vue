<script setup>
import { ref } from "vue";

// Basic Data

const firstName = "Bo ?";
const message = ref("Hi gwapa nako nga asawa");

//number identifyer
const number = ref("");
const result = ref("");
function checkNumber() {
  if (number.value === "") {
    result.value = "Please enter a number";
    return;
  }

  if (number.value % 2 == 0) {
    result.value = `${number.value} is an Even number.`;
  } else {
    result.value = `${number.value} is an Odd number`;
  }
}

// Counter
const count = ref(0);

const increase = () => {
  count.value++;
};

const decrease = () => {
  count.value--;
};

// Product

const price = 29;
const quantity = 5;

// Image & Link
const image =
  "https://media.istockphoto.com/id/538665020/photo/internet-meme-why-you-no-rage-face-3d-illustration.jpg?s=612x612&w=0&k=20&c=5D_g8Jy8kqg5Op2bb4RvcH8_6y0HGPqt29TKDrEqLyM=";

const web =
  "https://www.google.com/webhp?hl=en&ictx=2&sa=X&ved=0ahUKEwj69K2Y7K2VAxU1n68BHQXOFT0QPQgL";

// Attribute Binding

const isDisabled = true;
const isActive = true;
const color = "yellow";
</script>

<template>
  <div>
    <h1>Nag computer ka {{ firstName }}</h1>

    <h2>Total: {{ price * quantity }}</h2>

    <hr />

    <!-- Counter -->
    <h3>Count: {{ count }}</h3>
    <button @click="increase">Add</button>
    <button @click="decrease">Minus</button>
    <hr />
    <h3>Number checker</h3>
    <input type="number" v-model="number" placeholder="Enter a number" />
    <button @click="checkNumber">Check</button>
    <p>{{ result }}</p>
    <hr />

    <!-- Message -->
    <h1>{{ message }}</h1>
    <button
      @click="
        message = 'pa kiss ko please kanang dugay mahuman bitaw nga kiss'
      ">
      Change Message
    </button>

    <hr />

    <!-- Image -->
    <img :src="image" alt="Meme Image" width="250" />

    <br /><br />

    <!-- Link -->
    <a :href="web" target="_blank">Open Google</a>

    <br /><br />

    <!-- Disabled Button -->
    <button :disabled="isDisabled">Press Me</button>

    <!-- Dynamic Class -->
    <p :class="{ active: isActive }">ERROR!</p>

    <!-- Dynamic Style -->
    <p :style="{ color: color }">Vue Example</p>
    <hr />
    <h2>Books</h2>
    <Book bookName="The Hobbit" author="J.R.R. Tolkien" :isSold="true" />
    <Book bookName="1984" author="George Orwell" :isSold="false" />
    <Book bookName="Clean Code" author="Robert C. Martin" :isSold="true" />
  </div>
</template>

<style>
.active {
  color: red;
  font-weight: bold;
}

img {
  border-radius: 10px;
  margin-top: 10px;
}

button {
  margin: 5px;
  padding: 8px 16px;
  color: rgb(0, 11, 7);
}

hr {
  margin: 20px 0;
}
</style>

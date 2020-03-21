<template>
        <div id="MyApp">
      <div class="product">
        <div class="product-image">
            <img v-bind:src="image">
        </div>

        <div class="product-info">
          <h1>Professor {{ name }}</h1>
          <p v-if="variants[id].classSize > 4">Plenty of room in this class</p>
          <p v-else-if=" variants[id].classSize > 0">Running out of space in the class</p>
          <p v-else>Out of space in the class</p>

          <ul>
            <li>{{ variants[id].detail1 }}</li>
            <li>{{ variants[id].detail2 }}</li>
            <li>{{ variants[id].detail3 }}</li>
          </ul>


          <button class="add" v-if="variants[id].classSize > 0" v-on:click="addClass">Add Class</button>
          <button class="remove" v-if="classes > 0" v-on:click="removeClass">Remove Class</button>

          <div class="cart">
            <p>Classes({{classes}})</p>
          </div>

        </div>

        <div class="names" v-for="variant in variants" :key="variant.variantId">
          <p @mouseover="updateProduct(variant.variantPhoto, variant.variantName, variant.variantId)">{{ variant.variantName }}</p>
        </div>

      </div>
      <div class="footer">
      <p>Thank you for grading kindly<br>github repo: <a href="https://github.com/bharden/vue-creative-project-fun.git">https://github.com/bharden/vue-creative-project-fun.git</a></p>
    </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
    name: 'John',
    image: 'images/Teach-one.jpg',
    inventory: 0,
    id: 1,
    variants: [
      {
        variantId: 0,
        variantName: 'John',
        variantPhoto: 'images/Teach-one.jpg',
        detail1: '100% pass rate',
        detail2: 'Take home tests',
        detail3: 'No Homework!!',
        classSize: 5,
      },
      {
        variantId: 1,
        variantName: 'Taylor',
        variantPhoto: 'images/Teach-two.jpg',
        detail1: '80% pass rate',
        detail2: 'Tests at testing center',
        detail3: 'Lots of Homework!!',
        classSize: 5,
      },
      {
        variantId: 2,
        variantName: 'Richard',
        variantPhoto: 'images/Teach-three.jpg',
        detail1: '95% pass rate',
        detail2: 'Four tests',
        detail3: 'Some Homework!!',
        classSize: 5,
      },
      {
        variantId: 3,
        variantName: 'Cintia',
        variantPhoto: 'images/Teach-four.jpg',
        detail1: '65% pass rate',
        detail2: 'Ten tests',
        detail3: 'Many essays!!',
        classSize: 5,
      },
      {
        variantId: 4,
        variantName: 'Mark',
        variantPhoto: 'images/Teach-five.jpg',
        detail1: '50% pass rate',
        detail2: 'No tests',
        detail3: 'No Essays!!',
        classSize: 5,
      },
      {
        variantId: 5,
        variantName: 'May',
        variantPhoto: 'images/Teach-six.jpg',
        detail1: '0% pass rate',
        detail2: 'Online',
        detail3: 'Online Chat room!!',
        classSize: 5,
      },
      {
        variantId: 6,
        variantName: 'Daisy',
        variantPhoto: 'images/Teach-seven.jpg',
        detail1: '20% pass rate',
        detail2: 'Big final',
        detail3: 'No Homework!!',
        classSize: 5,
      },
      {
        variantId: 7,
        variantName: 'Spencer',
        variantPhoto: 'images/Teach-eight.jpg',
        detail1: '100% pass rate',
        detail2: 'Some tests',
        detail3: 'Long Homework!!',
        classSize: 5,
      },
      {
        variantId: 8,
        variantName: 'Melvan',
        variantPhoto: 'images/Teach-nine.jpg',
        detail1: '55% pass rate',
        detail2: 'Really hard tests',
        detail3: 'No Corona!!',
        classSize: 5,
      },
      {
        variantId: 9,
        variantName: 'Luther',
        variantPhoto: 'images/Teach-ten.jpg',
        detail1: '70% pass rate',
        detail2: 'No tests',
        detail3: 'No Earthquake!!',
        classSize: 5,
      }
    ],
    classes: 0,
    }
  },
  methods: {
    addClass() {
      this.classes += 1,
      this.variants[this.id].classSize -=1
    },
    updateProduct(variantPhoto, variantName, variantId) {
      this.image = variantPhoto,
      this.name = variantName,
      this.id = variantId
    },
    removeClass() {
      this.classes -= 1,
      this.variants[this.id].classSize +=1
    },
  },
}
</script>
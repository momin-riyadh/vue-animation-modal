<template>
  <div class="home">
    <button @click="toggleModal">Open</button>

    <transition name="fade">
      <div v-if="isOpen" class="modal">
        <button @click="toggleModal">Close</button>

        <div>
          <h2>Lorem ipsum dolor sit amet.</h2>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Assumenda atque beatae consectetur dignissimos distinctio esse explicabo facere facilis fuga fugiat, laborum magnam minus molestias nemo odit praesentium repellat reprehenderit tenetur.
        </div>
      </div>
    </transition>


  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggleModal() {
      this.isOpen = !this.isOpen
    }
  }
}
</script>

<style>
  .fade-enter{
    opacity: 0;
  }

  .fade-enter-active,
  .fade-leave-active{
    transition: opacity 0.5s ease-in-out;
  }

  .fade-leave-to{
    opacity:0;
  }
</style>

<template>
  <div class="my-toast">
    abc
  </div>
</template>

<script>
export default {
  setup (props) {
    console.log('props: ', props);
    const showAlert = () => {
      alert('asdkasd')
    }

    return {
      showAlert
    }
  }
}
</script>

<style>
.my-toast {
  /* background-color: red; */
  color: white;
}
</style>
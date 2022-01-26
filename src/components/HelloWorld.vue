<template>
  <div class="hello">
    <button @click="toast">Toast it!</button>
  </div>
</template>

<script>
import { createToast, withProps,  } from 'mosha-vue-toastify';
import 'mosha-vue-toastify/dist/style.css'
import CustomizedContent from "./CustomizedContent.vue";

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup () {
    const toast = () => {
      withProps
        createToast(withProps(CustomizedContent, { yourFavProp: 'bruh' }),
        {
            type: 'info',
            position: 'top-center',
            timeout: 2000,
            transition: 'slide',
            hideProgressBar: true,
            showCloseButton: false,
            toastBackgroundColor: '#333333'
          })
      //   createToast(
      //     {
      //       title: '已加入自選股'}, 
      //       {
      //       type: 'info',
      //       position: 'top-center',
      //       timeout: 2000,
      //       transition: 'slide',
      //       hideProgressBar: true,
      //       showCloseButton: false,
      //       toastBackgroundColor: '#333333'
      //     }
      // )
    }
    return { toast }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >

.mosha__toast {
  min-width: 100px;
  min-height: 20px;
  padding: 6px 8px;
  /* top: 50% !important; */
}

.mosha__toast .mosha__toast__content__text {
  font-size: 14px;

}
</style>

<template >
  <div>

    <form w-75 @submit.prevent >
      <my-input v-model="comment.name" class="form-control" placeholder="name" />
      <my-input v-model="comment.email" class="form-control my-3" placeholder="Email" />
      <my-input v-model="comment.content" class="form-control" placeholder="Content" />
      <my-button @click="createComment" class="btn btn-primary mt-3">Send...</my-button>
    </form>

  </div>
</template>

<script>
import MyButton from './UI/MyButton.vue';
export default {
  components: { MyButton },
  data() {
    return {
       comment: {
           name: "",
           email: "",
           content: "",
       }
    }
  },
  methods: {
    createComment() {
         this.comment.id = Date.now();
          this.$emit("addComment", this.comment);
          this.comment = {
            name: '',
            email: '',
            content: '',
          }
         
    }
  },
}
</script>

<style >
  
</style>


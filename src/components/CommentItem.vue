<template >
  <div class="comment">
  <div>
    <p>{{comment.name}} :<b>{{comment.email}}</b></p>
        <p><b>Content:</b>{{comment.content}}</p>
  </div>
    <my-button class="btn btn-danger">Delete</my-button>
  </div>
</template>

<script>

export default {
  props: {
    comment: {
      type:Object,
      required: true,
    }
  },
}
</script>

<style >
  .comment {
    border:1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>
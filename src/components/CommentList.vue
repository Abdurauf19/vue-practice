<template>
  <div>
    
    <comment-item class="mx-auto comment"
     v-for="comment in comments" 
     :comment="comment"
     :key="comment.key"/>
       
    

  </div>
</template>

<script>
 import CommentItem from '../components/CommentItem'
export default {

   components : {
    CommentItem
  },

  props: {
    comments: {
      type: Array,
      required: true
    }
  },
  
}
</script>

<style >
.comment {
        border: 5px solid #ccc;
        padding: 10px;
        margin: 10px;
    }
</style> >
  

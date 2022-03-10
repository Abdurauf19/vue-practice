<template>
    <div>
        <comment-form @addComment="createComment" />
        <comment-list :comments="comments"/>
    </div>
</template>

<script>
import CommentForm from './components/CommentForm';
import CommentList from './components/CommentList';


export default {  
    components: {
        CommentForm,
        CommentList
    },
    data() {
        return {
           comments:[{ id: 0, name: this.name, email: this.email, content: this.content}],
        }
    },

    methods: {
      createComment(commnet) {
         this.comments.push(commnet)
      }
    },
}
</script>

<style >
    
</style>
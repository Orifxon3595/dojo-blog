<template>
  <div>
    Details
    <div v-if="post">
        <h3>{{ post.title }}</h3>
    </div>
  </div>
</template>

<script>
import getPost from '../composables/getPost'
export default {
    props: ['id'],
    setup(props){
        const {post, error, load} = getPost(props.id);

        load()

        return{post, error}
    }
}
</script>

<style>

</style>
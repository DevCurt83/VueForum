<!-- here the template, script + style form the SFC.. Single file component
// which is a special vue file which allow us to have template, javascript + CSS in one file 
// visit vuejs.org/v2/style-guide/#Rule-Categories for advise on naming components -->
<template>
    <div><p>Hello World, How goes? :)</p></div>
    <div v-for="thread in threads" :key="thread.id"> <!-- whenever rendering a list of attributes, you should pass a key so vue can keep track of the list, each key should be unique -->
        <h2>{{thread.title}}</h2>
        <div v-for="postId in thread.posts" :key="postId">       <!-- remember the importance of the key here -->
             <p>{{users.find(u => u.id === posts.find(p => p.id === postId).userId).name}}</p>
             <p>{{posts.find(p => p.id === postId).text}}</p>    <!-- here we search in posts array for post with corresponding ID -->
        </div> 
    </div>
</template>

<script> //here we want to import our user data
import sourceData from "@/data.json"
export default {
    data () {
        return {
            threads: sourceData.threads,
            posts: sourceData.posts,
            users: sourceData.users
        }
    }
}
</script>

<style scoped>

</style>



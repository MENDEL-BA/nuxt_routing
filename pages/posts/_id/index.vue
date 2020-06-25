<template>
    <div>
        <h1> {{posts.title}}</h1>
        <p>{{ posts.content }}</p>
    </div>
</template>

<script>
export default {
    
    data : () => ({
       posts : {
           title : '',
           content : '',
           slug : ''
       }
    }),

    mounted() {
        // this.slug = this.$route.params.id;
    //    this.posts =  this.$store.state.posts.find (post =>
    //         post.slug === this.$route.params.id
    //     )
    },

    async asyncData({store, route}) {
        await store.dispatch('all', [
            {
                 title : 'Article 1',
                 slug : 'article-1',
                 content : 'coucou mendel 1'
            },
            {
                 title : 'Article 2',
                 slug : 'article-2',
                 content : 'coucou mendel 2'
            } 
      ])

       return { posts : store.state.posts.find (post => post.slug === route.params.id)}
    
    }
}
</script>

<style scoped>
    
</style>
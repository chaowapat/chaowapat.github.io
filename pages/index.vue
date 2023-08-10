<template>
    <div>
        <b-row>
            <b-col v-for="post in posts" :key="post.slug">
                <b-card 
                    :title="post.title" 
                    tag="article" 
                    style="max-width: 20rem" 
                    class="mb-2"
                    >
                    <b-card-text>
                        <!-- Some quick example text to build on the card title and make up the bulk of the card's content. -->
                        {{ post.description }}
                    </b-card-text>

                    <b-button :to="{name: 'posts-slug', params:{ slug: post.slug } }" 
                    variant="primary"
                    >Go somewhere</b-button>
                </b-card>
            </b-col>
        </b-row>
    </div>
</template>
<!-- img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top -->

<script>

export default {
    // setup () {
    async asyncData({ $content }) {
        const postsData = await $content('posts').fetch();
        return {
            posts: postsData,
        };
    },
    mounted() {
        // console.log('THIS.POSTS', this.posts);
    },
    // }
};
</script>

<style lang="css" scoped></style>


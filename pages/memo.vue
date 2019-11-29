<template>
    <div>
        <div class="columns">
            <div v-for="(post,index) in posts" :key="post.slug + '_' + index" class="column">
                <div class="box">
                    <article class="media">
                        <div class="media-content">
                            <div class="content">
                                <strong>{{ post.title }}</strong>
                                <br/>
                                {{ post.summary }}
                            </div>
                            <nav class="level is-mobile">
                                <div class="level-left">
                                    <router-link :to="'/posts/' + post.slug" class="level-item">
                                        <span class="icon is-small">
                                            <i class="fa fa-arrow-right"></i>
                                        </span>
                                    </router-link>
                                </div>
                                <div class="level-right">
                                    <div class="tags">
                                        <span v-for="(tag,index) in post.tags" :key="tag.slug + '_' + index" class="tag">{{ tag.name }}</span>
                                    </div>
                                </div>
                            </nav>
                        </div>
                    </article>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import {butter} from '@/buttercms'

    export default {
        name: "memo",
        data() {
            return {
                posts: []
            }
        },
        methods: {
            getPosts() {
                butter.post.list({
                    page: 1,
                    page_size: 10,
                    category_slug: 'portfolio'
                }).then(res => {
                    this.posts = res.data.data
                })
            }
        },
        created() {
            this.getPosts()
        }
    }
</script>

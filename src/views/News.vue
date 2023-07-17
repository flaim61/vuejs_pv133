<template>
    <section class="posts">
        <div v-for="(post, index) in this.posts" v-if='this.posts.length' class="post">
            <h3>
                {{ post.title }}
            </h3>
            <p>
                {{ post.text }}
            </p>
        </div>
        <div v-else>
            <div class="empty">
                Пока еще нет ни одного поста!
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "News",
        components: {
            
        },
        data(){
            return {
                posts: [
                    { id: 1, title: "Пост 1", text: "Какое-то тестовый текст 1"},
                    { id: 2, title: "Пост 2", text: "Какое-то тестовый текст 2"},
                    { id: 3, title: "Пост 3", text: "Какое-то тестовый текст 3"},
                    { id: 4, title: "Пост 4", text: "Какое-то тестовый текст 4"},
                    { id: 5, title: "Пост 5", text: "Какое-то тестовый текст 5"},
                    { id: 6, title: "Пост 6", text: "Какое-то тестовый текст 6"},
                    { id: 7, title: "Пост 7", text: "Какое-то тестовый текст 7"},
                ]
            }
        }
    }
</script>

<style>
    .posts{
        margin: 0 auto;
        max-width: 80%;
    }
    .post{
        border: 1px solid black;
        padding: 15px;
        margin-top: 10px;
    }
    .post:last-child{
        margin-bottom: 10px;
    }
    .empty{
        margin-top: 10px;
        margin-bottom: 10px;
        padding: 15px;
        text-align: center;
    }
</style>
<template>
    <div class="container">
        <h1>Reaction Time Scores</h1>
        <h1 style="border: 2px dotted black; margin: 20px;">{{ score }} ms</h1>
        <p>{{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'I am The Flash'
        } else if (this.score < 400) {
            this.rank = 'I am Gundala'
        } else {
            this.rank = 'I am The Arrow'
        }
    },
}
</script>

<style>
    .container {
        border: 2px dashed black;
        margin: 50px 200px;
        background-color: pink;
    }
</style>
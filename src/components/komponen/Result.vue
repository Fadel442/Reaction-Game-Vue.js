<template>
    <div class="container">
        <h1>Reaction Time Scores</h1>
        <h1 style="border: 2px dotted black; margin: 20px;">{{ score }}</h1>

    </div>
</template>

<script>
export default {
    props: ['score']
}
</script>

<style>
    .container {
        border: 2px dashed black;
        margin: 50px 200px;
        background-color: pink;
    }
</style>
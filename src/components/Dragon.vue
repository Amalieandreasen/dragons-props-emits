<script setup>
const props = defineProps({
    dragon:Object
})

const dragonName = defineModel();

const emit = defineEmits(['superEvent'])
const{
    name,Skills, img_url } = props.dragon

</script>

<template>
    <article>
        <p class="name">{{ name }}</p>
        <p class="skills">{{ Skills}}</p>
        <img :src=" img_url " :alt="name">
        <form>
    <label for="betterName">Rename to:</label>
    <input v-model="dragonName" type="text" placeholder="Better name..." id="betterName" required>
    <input type="submit" value="Update name" />
  </form>
    </article>
</template>

<style scoped>
article{
    box-shadow: 0 0 3px 1px rgba(0, 0, 0, 0.5);
    border-radius: 6px;
    padding: 10px;
}

img{
    width: 100%;
}
</style>
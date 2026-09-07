<script setup>
    import { ref } from 'vue'

    const img = ref('/assets/me.png')
    const imgWidth = ref(450)
    const imgHeight = ref(280)

</script>

<template>

    <div>
        <img :src="img" :width="imgWidth" :height="imgHeight" />
    </div>
</template>

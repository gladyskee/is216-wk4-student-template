<script setup>
    import { ref } from 'vue'

    const img1 = ref('/assets/me.png')
    const imgWidth1 = ref(450)
    const imgHeight1 = ref(280)

    const img2Attrs = ref({
        src: '/assets/me.png',
        width: 450,
        height: 280
    })
</script>

<template>
    <div>
        <img :src="img1" :width="imgWidth1" :height="imgHeight1" />

        <img v-bind="img2Attrs" />
    </div>
</template>


<script>
export default {
    props: ['title']
}
</script>

<template>
    <h1 class="text-4xl font-bold text-center text-red-800">

        <p>
            <slot></slot>
        </p>
    </h1>
</template>
<template>
  <div id="navbar" class="w-100">
    <nav class="navbar bg-light bg-dark text-light h-45">
        <div class="container-fluid">
            <i class="fa-solid fa-bars fa-lg m-2" @click="openMenu()"></i>
        </div>
    </nav>
  </div>
</template>

<script>
export default {
    props: {
        isExpanded: {
            Type: Boolean
        }
    },
    methods: {
        openMenu() {
            this.$emit('open-menu', !this.$props.isExpanded);
        }
    },
}
</script>

<style>

</style>
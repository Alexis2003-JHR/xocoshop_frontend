<template>
    <div class="slide">
        <transition name="slide">
            <slot />
        </transition>
    </div>
</template>

<script>
export default {}
</script>

<style>
/*Animation*/
.slide-enter-active,
.slide-leave-active{
    transition: opacity 0.7s ease-in-out;
}
.side-enter-from,
.slide-leave-to{
    opacity: 0;
}
.slide-enter-to,
.slide-leave-from{
    opacity: 1;
}
</style>
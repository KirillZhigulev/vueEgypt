<script setup lang="ts">
import { ref, onMounted } from 'vue'

const wrapper = ref<null | HTMLElement>(null) 
const options = {
    threshold: 0.5,
}
onMounted(() => {
    const observer = new IntersectionObserver((entries) => {    
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
             wrapper.value?.classList.add('animated');  
            setTimeout(() => {  
                wrapper.value?.classList.add('hoverAdded');
            },2000);
            } else {
             wrapper.value?.classList.remove('animated');
             wrapper.value?.classList.remove('hoverAdded');
            }
    });
        
    }, options)
    
 if(wrapper.value)observer.observe(wrapper.value)
})

</script>

<template>

<div class="root">
    <div ref="wrapper"class="h2">
        путешествие
        
        <span class="believe first">путешествие</span>
        <span class="believe second">путешествие</span>
        <span class="third">в солнечный Египет</span>

    </div>
</div>
</template>

<style lang="sass" scoped>
@import '../main.sass'

@keyframes pushTopEffect 
    0%, 100%
        top:0 
    50%
        top: -20px

@keyframes pushBottomEffect 
    0%, 100%
        top:0 
    50%
        top: 20px

@keyframes showEffect 
    0%, 100%
        transform: translateY(-50%) scaleY(0)
    50%
        transform: translateY(-50%) scaleY(1)
         
.root 
    position: relative
    height: 100vh
    font-family: "Cookie", cursive

.h2 
    position: absolute
    top: 50%
    left: 50%
    font-size: 12em
    font-weight: 900
    text-transform: uppercase
    color: transparent
    transform: translate(-50%, -50%)

.believe
    position: absolute
    top: 0
    left: 0
    color: $black  
    transition:  0.5s
    overflow: hidden

    &.first
        clip-path: polygon(0 0, 100% 0, 100% 50%, 0 50%)
    &.second
        clip-path: polygon(0 50%, 100% 50%, 100% 100%, 0 100%)

.third
    position: absolute
    top: 50%
    left: 0
    margin-left: 10px
    width: calc(100% - 10px)
    font-size: 0.35em
    font-weight: 500
    letter-spacing: 0.3em
    text-align: center
    color: $white
    background-color: #ff0
    transition: 0.5s
    transform: translateY(-50%) scaleY(0)

.h2.hoverAdded:hover

    .first
        transform: translateY(-20px) 

    .second
        transform: translateY(20px)

    .third
        transform: translateY(-50%) scaleY(1)

.h2.animated

    .first
        animation: pushTopEffect 1s ease 0.5s 1

    .second
        animation: pushBottomEffect 1s ease 0.5s 1

    .third
        animation: showEffect 1s ease 0.5s 1

</style>

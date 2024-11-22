<script setup>
import {ref} from 'vue'

const name= "Pepito"
let counter = ref(5)
let characters = ref([])
function add(){
    counter.value++
    console.log(counter)
    characters.value.push(counter.value)
}

function rest(){
    counter.value--
    console.log(counter)

}
console.log("Hola mundo", name)
</script>

<template>
    <div class="bg-purple-300 max-w-96 rounded py-4 px-6 mx-auto">
        Hola{{ name }}
        <div 
         v-if="counter >0" 
        class="bg-red-500 text-white size-7 rounded-full flex items-center justify-center">
            {{ counter }}
        </div>
        <div v-else >
            Nadie te escribe 😪</div>
        <div 
        @click="add()"
        class="bg-blue-500 text-white size-7 rounded-full flex items-center justify-center">+
            {{ }}
        </div>
        <div 
        @click="rest()"
        class="bg-black text-white size-7 rounded-full flex items-center justify-center">-
            {{ }}
        </div>
    </div>

    <div
    v-for="(name, index) in characters"
    :key="index"
     class="bg-green-500 mb-1">
     {{ name }}
    </div>
    
    
    
</template>
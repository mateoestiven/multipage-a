<script setup >

    import { ref } from 'vue'

    let number = ref(5);
    
    function add(){
        number.value++;
    }

    function remove(){
        if(number.value > 0){
            number.value--; 
        }
    }
</script>

<template>
    <div class="max-w-96 bg-blue-700 rounded py-3 px-6 mx-auto">
        <div 
        class="bg-red-400 size-8 flex items-center mx-auto justify-center rounded-full"
        v-if="number > 0"
        >
            {{ number }}
        </div>

        <div 
        class=""
        v-else>
            Nadie te escribe :/
        </div>

        <div class=" flex justify-between">
            <div class="bg-purple-400 size-8 flex items-center  justify-center rounded-full hover:cursor-pointer" @click="add()"> 
                 +
        </div>
             <div class="bg-purple-400 size-8 flex items-center justify-center rounded-full hover:cursor-pointer " @click="remove()" >
                 -
             </div>
        </div>
        
    </div>
</template>


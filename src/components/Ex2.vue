<script>
    export default { 
        // Add code in appropriate places
        data() {

            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                Name : ""
            }
            
        },
        methods :{
            del(idx){
                console.log(idx)
                return this.items.splice(idx, 1)

            },

            AddItem(){
                return this.items.push(this.Name)
                
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for = "item, idx in items">{{ item }}<button v-on:click="del(idx)">Delete</button></li>
     </ul>

     <div>
        <input type="text" v-model="Name"></input>
        <button v-on:click="AddItem()">Add!</button>
     </div>
   
</template>

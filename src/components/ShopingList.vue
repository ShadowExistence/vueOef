<template>
<h2>Shopping List</h2>
<div>
    <input @keypress.enter="add()" type="text" name="items" id="name1">
    <ul>
        <li v-bind:key="(item,n)" v-for="(item, n) in shoppingList">
            <span>
            <input class="form-check-input" type="checkbox" value="" v-model="item.checked">
             {{item.name}}
            </span>
        </li>
    </ul>
    <button @click="clearAll()">Clear List</button>
</div>
    
</template>

<script>

export default {
    name:'ShoppingList',
    data(){
        return{
            shoppingList:[]
        }
        
    },
    methods:{
        add(){
            const name = document.getElementById('name1').value
            console.log(name)
            if(name !== ""){
                this.shoppingList.push({name: name})
            }
        },
        clearAll(){
            this.shoppingList = []
        },
        remove(){
            this.shoppingList
        }
    }
}
</script>

<style>

</style>
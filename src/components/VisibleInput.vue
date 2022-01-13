<template>
    <div>
        <h2>VisibleInput</h2>
        <input :type="this.visible? 'text' : 'password' " v-bind:value="msg" />
        <input @click="this.visible = !this.visible" type="button" value="X">
    </div>
</template>

<script>
export default {
    name: 'VisibleInput',
    props:{
        msg: String
    },
    data(){
        return{
            visible: false
        }
    }
}
</script>


<template>
    <div style="width:50%">
        <ul class="nav nav-tabs">
            <li
                v-for="(tab,idx) in tabs"
                :key="idx"
                class="nav-item">
                <a
                    class="nav-link"
                    :class="{active:tab===selected}"
                    @click="setTab(tab)">
                    {{tab}}
                </a>
            </li>

        </ul>
        <slot></slot>
    </div>
</template>
<script>
export default{
    props:{
        tabs:{
            type:Array,
            required:true,
        },
        selected:{
            type:String,
            required:true,
        }
    },
    methods:{
        setTab(tab){
            this.$emit('selected', tab);
        }
    }
}

</script>
<style scoped>
.nav-link.active{
    color:red;
}

</style>

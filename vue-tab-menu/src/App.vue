<template>
    <div id="app">
        <TabNav
            :tabs="['Home', 'Settings', 'Profile']"
            :selected="selected"
            @selected="setSelected">

            <Tab :isSelected="selected === 'Home'">
                <p>This is Home</p>
            </Tab>
            <Tab :isSelected="selected === 'Settings'">
                <p>This is Settings</p>
            </Tab>
            <Tab :isSelected="selected === 'Profile'">
                <p>This is Profile</p>
            </Tab>
        </TabNav>
    </div>
</template>

<script>
import TabNav from "./components/TabNav";
import Tab from "./components/Tab";

export default {
    data(){
        return{
            selected:'Home'
        }
    },
    components:{
        Tab,
        TabNav
    },
    methods:{
        setSelected(tab){
            this.selected=tab;
        }
    }
}
</script>

<style>
body{
    background-color: #45443F;
    color:#fefefe;
}
th, td{
    padding:5px;
    border:1px solid #fff;
}

</style>

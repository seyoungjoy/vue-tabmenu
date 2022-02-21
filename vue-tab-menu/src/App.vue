<template>
    <div id="app">
        <TabNav
            :tabs="['Home', 'Setting', 'Profile']"
            :selected="selected"
            @selected="setSelected"
        >
            <Tab :isSelected="selected === 'Home'">
                <p>Some test text</p>

            </Tab>
            <Tab :isSelected="selected === 'Settings'">
                <h1>more test text</h1>
            </Tab>
            <Tab :isSelected="selected === 'Profile'">
                <ul>
                    <li>list test1</li>
                    <li>list test2</li>
                    <li>list test3</li>
                    <li>list test4</li>
                </ul>
            </Tab>

        </TabNav>

    </div>
</template>

<script>

import TabNav from "@/components/TabNav";
import Tab from "@/components/Tab";

export default {
    name: 'App',
    data(){
      return{
          selected:'Home'
      }
    },
    components: {
        Tab,
        TabNav
    },
    methods:{
        setSelected(tab){
            this.selected = tab;
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

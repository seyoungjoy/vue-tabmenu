<template>
    <div v-if="isSelected">
    <!-- isSelected 값이 참일때만 보임. selected의 값이 home일때만 보임. -->
        <slot></slot>

    </div>
</template>
<script>
export default {
    props:{
        isSelected:{
            type:Boolean
        }
    }

}

</script>

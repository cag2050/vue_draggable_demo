<template>
<div>
    <draggable :list="list" class="dragArea" @start="startFunc">
        <div v-for="element in list" class="ele">{{element.name}}</div>
    </draggable>
</div>
</template>

<script>
import draggable from 'vuedraggable'

export default {
    components: {
        draggable
    },
    data () {
        return {
            list: [ {name: '1'}, {name: '2'}, {name: '3'}, {name: '4'}, {name: '5'}, {name: '6'} ]
        }
    },
    methods: {
        startFunc: function (evt) {
            console.log(evt)
            console.log('start')
        }
    }
}
</script>

<style>
.ele {
    width: 200px;
    float: left;
    background-color: yellow;
    margin: 10px;
}
</style>

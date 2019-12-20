<template>
    <div class="view-lines">
        <div v-for="line in lines" v-bind:key="line.index">
            <view-Line :line-data="line.lineData"></view-Line>
        </div>
    </div> 
</template>

<script>
import { ViewLine } from "./ViewLine";
export default {
    name: "ViewLines",
    data () {
        return {
        };
    },
    props: {
        linesData: {
            type: Array,
            default: () => {
                return [];
            }
        }
    },
    components: {
        ViewLine
    },
    mounted () {
        console.log('ViewLines');
        console.log(this.linesData);
    }
}
</script>

<style>

</style>
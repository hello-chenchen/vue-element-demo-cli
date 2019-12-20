<template>
    <div class="view-line">
        <span class="span-line">{{ lineData.message }}</span>
    </div>
</template>

<script>
import { LineType } from "./../common/LineType";
export default {
    name: "ViewLine",
    data () {
        return {};
    },
    props : {
        lineData: {
            type: Object,
            default: () => {
                return {
                    type: LineType.info,
                    message: ''
                };
            }
        }
    },
    mounted () {
        console.log('ViewLine');
        console.log(this.lineData);
    }
}
</script>

<style>

</style>
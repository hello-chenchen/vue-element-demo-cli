<template>
    <div class="view-line">
        <span class="span-line">{{ lineData.message }}</span>
    </div>
</template>

<script>
import { LineType } from "./VisualLogType"
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
    }
}
</script>

<style>
.span-line {
    display: block;
    text-align: left;
}
</style>
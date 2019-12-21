<template>
    <div class="view-content">
        <view-Lines :lines-data="contentData.viewData"></view-Lines>
    </div>
</template>
<script>
import ViewLines from "./ViewLines.vue";
export default {
    name: "ViewContent",
    data () {
        return {};
    },
    props: {
        contentData: {
            type: Object,
            default: () => {
                return {
                    options:{},
                    viewData:[]
                };
            }
        }
    },
    components: {
        ViewLines
    },
    mounted () {
    }
}
</script>
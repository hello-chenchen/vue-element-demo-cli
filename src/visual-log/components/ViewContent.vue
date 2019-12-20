<template>
    <div class="view-content">
        <view-Lines :lines-data="viewContentData"></view-Lines>
    </div>
</template>
<script>
import { ViewLines } from "./ViewLines";
export default {
    name: "ViewContent",
    data () {
        return {};
    },
    props: {
        viewContentData: {
            type: Object,
            default: () => {
                return {};
            }
        }
    },
    components: {
        ViewLines
    },
    mounted () {
        console.log('ViewContent');
        console.log(this.viewContentData);
    }
}
</script>
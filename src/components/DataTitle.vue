<template>
    <div class="">
        <h2 class="">{{ text }}</h2>
        <div class="">
            {{ timestamp }}
        </div>
    </div>
</template>

<script>
import moment from 'moment'

export default {
    name: 'DataTitle',
    props: ['text', 'dataDate'],
    computed: {
        timestamp: function() {
            return moment(this.dataDate).format('MMMM Do YYYY, h:mm:ss a')
        }
    }
}
</script>

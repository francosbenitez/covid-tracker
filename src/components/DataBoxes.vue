<template>
    <div class="row">
        <div class="col">
            <b-card>
                <h1>Cases</h1>
                <span>New:</span>
                {{ numberWithCommas(stats.NewConfirmed) }}
                <span>Total:</span>
                {{ numberWithCommas(stats.TotalConfirmed) }}
            </b-card>

            <b-card>
                <h1>Deaths</h1>
                <span>New:</span>
                {{ numberWithCommas(stats.NewDeaths) }}
                <span>Total:</span>
                {{ numberWithCommas(stats.TotalDeaths) }}
            </b-card>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DataBoxes',
    props: ['stats'],
    methods: {
        numberWithCommas(x) {
            return x.toString()
                .replace(/\B(?=(\d{3})+(?!\d))/g, ',');
        }
    }
}
</script>

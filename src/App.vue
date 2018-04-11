<template>
    <div class="container">
        <new-quote @quoteAdded="newQuote"></new-quote>
        <quote-grid :quotes="quotes"></quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">
                    Info: Click on a quote to delete it.
                </div>
            </div>

        </div>
    </div>
</template>

<script>
import quoteGrid from './components/QuoteGrid.vue';
import newQuote from './components/NewQuote.vue';

export default {
    data: function() {
        return {
            quotes: ['The default quote'],
            maxQuotes: 10,
        };
    },
    methods: {
        newQuote(quote) {
            this.quotes.push(quote);
        },
    },
    components: {
        quoteGrid,
        newQuote,
    },
};
</script>

<style>
</style>

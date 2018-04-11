<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <new-quote @quoteAdded="newQuote"></new-quote>
        <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
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
import appHeader from './components/Header.vue';

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
        deleteQuote(index) {
            this.quotes.splice(index, 1);
        },
    },
    components: {
        quoteGrid,
        newQuote,
        appHeader,
    },
};
</script>

<style>
</style>

<template>
    <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid :quotes="quotes" @quoteDeleted="quoteDeleted"></app-quote-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on Quote to delete it !</div>
            </div>
        </div>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';
    import Header from './components/Header.vue'

    export default {
        data: function(){
            return {
                quotes: [
                    'just a Quote to see something'
                ],
                maxQuotes: 10
            }
        },
        methods: {
            newQuote(quote){
                if(this.quotes.length>= this.maxQuotes){
                    return alert('Please delete Quotes first!')
                }
                this.quotes.push(quote);
            },
            quoteDeleted(index){
                this.quotes.splice(index,1);
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote,
            appHeader: Header
        }
        
    }
</script>

<style>
</style>
<template>
    <div>
        <app-stock v-for="stock in stocks" v-bind:key="stock.id"></app-stock>
    </div>
</template>
<script>
import Stock from './Stock.vue'
export default {
    data(){
        return {
            stocks: [
                {id:1, name: 'BMW' , price: 110},
                {id:2, name: 'Tesla' , price: 110},
                {id:3, name: 'Ford' , price: 110},
                {id:4, name: 'Renault' , price: 110},
            ]
        }
    },
    components: {
        appStock :Stock
    }
}
</script>
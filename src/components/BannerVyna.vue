<template>
    <section class="women-banner spad">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-12 mt-5" v-if="products.length > 0">
                    <carousel class="product-slider" :items="3" :nav="false" :autoplay="false"> 

                        <div class="product-item" v-for="itemProduct in products" v-bind:key="itemProduct.id">
                            <div class="pi-pic">
                                <router-link v-bind:to="'/product/'+itemProduct.id"><img v-bind:src="itemProduct.galleries[0].photo" alt="" /></router-link>
                                <ul>
                                    <li class="w-icon active">
                                        <router-link v-bind:to="'/product/'+itemProduct.id"><i class="icon_bag_alt"></i></router-link>
                                    </li>
                                    <li class="quick-view"><router-link v-bind:to="'/product/'+itemProduct.id">+ Quick View</router-link></li>
                                </ul>
                            </div>
                            <div class="pi-text">
                                <div class="catagory-name">{{ itemProduct.type }}</div>
                                <a href="#">
                                    <h5>{{ itemProduct.name }}</h5>
                                </a>
                                <div class="product-price">
                                    ${{ itemProduct.price }}.00
                                    <span>$35.00</span>
                                </div>
                            </div>
                        </div>
                        
                    </carousel>
                </div>

                <div class="col-lg-12" v-else>
                <p>
                    Product belum tersedia.    
                </p>                
                </div>
    
            </div>
        </div>
    </section>
</template>

<script>
import carousel from 'vue-owl-carousel';
import axios from "axios";

export default {
    name: 'BannerVyna',
    components: {
        carousel
    },
    data() {
        return {
            products: []
        };
    },
    mounted() {
        axios
        .get("http://learn-laravue.test/api/products")
        .then(res => (this.products = res.data.data.data))
        // eslint-disable-next-line no-console
        .catch(err => console.log(err));
    }
}
</script>

<style scoped>
.product-item {
    margin-right: 20px;
}
</style>
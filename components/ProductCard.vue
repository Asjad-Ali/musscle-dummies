<template>
  <div class="container">
    <div class="row">
        <div class="col-md-3 col-sm-6">
            <div class="product-grid">
                <div class="product-image">
                    <a href="#" class="image">
                        <img class="pic-1" src="/women.jpeg">
                        <img class="pic-2" src="/man.jpeg">
                    </a>
                     <span class="product-sale-label">sale!</span>
                    <ul class="social">
                        <li><a href="#" data-tip="Quick View"><i class="fa fa-eye"></i></a></li>
                        <li><a href="#" data-tip="Add to wishlist"><i class="fa fa-heart"></i></a></li>
                    </ul>
                    <div class="product-rating">
                        <ul class="rating">
                            <li class="fas fa-star"></li>
                            <li class="fas fa-star"></li>
                            <li class="fas fa-star"></li>
                            <li class="far fa-star"></li>
                            <li class="far fa-star"></li>
                        </ul>
                        <a class="add-to-cart" href="#"> ADD TO CART </a>
                    </div>
                </div>
                <div class="product-content">
                    <h3 class="title"><a href="#">Men's Shirt</a></h3>
                    <div class="price"><span>$28.00</span>$20.00</div>
                </div>
            </div>
        </div>
        <div class="col-md-3 col-sm-6">
            <div class="product-grid">
                <div class="product-image">
                    <a href="#" class="image">
                        <img class="pic-1" src="images/img-3.jpg">
                        <img class="pic-2" src="images/img-4.jpg">
                    </a>
                    <ul class="social">
                        <li><a href="#" data-tip="Quick View"><i class="fa fa-eye"></i></a></li>
                        <li><a href="#" data-tip="Add to wishlist"><i class="fa fa-heart"></i></a></li>
                    </ul>
                    <div class="product-rating">
                        <ul class="rating">
                            <li class="fas fa-star"></li>
                            <li class="fas fa-star"></li>
                            <li class="fas fa-star"></li>
                            <li class="far fa-star"></li>
                            <li class="far fa-star"></li>
                        </ul>
                        <a class="add-to-cart" href="#"> ADD TO CART </a>
                    </div>
                </div>
                <div class="product-content">
                    <h3 class="title"><a href="#">Women's Tshirt</a></h3>
                    <div class="price">$19.00</div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script setup>

</script>

<style scoped>
.product-grid{
    font-family: 'Roboto', sans-serif;
    text-align: center;
    transition: all 0.5s;
}
.product-grid:hover{ box-shadow: 0 5px 18px rgba(0, 0, 0, 0.3); }
.product-grid .product-image{
    position: relative;
    overflow: hidden;
}
.product-grid .product-image a.image{ display: block; }
.product-grid .product-image img{
    width: 100%;
    height: auto;
}
.product-image .pic-1{
    opacity: 1;
    backface-visibility: hidden;
    transition: all 0.5s;
}
.product-grid:hover .product-image .pic-1{ opacity: 0; }
.product-image .pic-2{
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    opacity: 0;
    position: absolute;
    top: 0;
    left: 0;
    transition: all 0.5s;
}
.product-grid:hover .product-image .pic-2{ opacity: 1; }
.product-grid .product-sale-label{
    color: #fff;
    background: #6da84a;
    font-size: 14px;
    font-style: italic;
    text-transform: uppercase;
    width: 55px;
    height: 55px;
    line-height: 55px;
    border-radius: 50px;
    position: absolute;
    top: 10px;
    left: 10px;
}
.product-grid .social{
    padding: 0;
    margin: 0;
    list-style: none;
    position: absolute;
    top: 15px;
    right: 7px;
}
.product-grid .social li{
    transform: translateX(60px);
    transition: all 0.3s ease 0.3s;
}
.product-grid .social li:nth-child(2){ transition: all 0.3s ease 0.4s; }
.product-grid:hover .social li{ transform: translateX(0); }
.product-grid .social li a{
    color: #707070;
    background: #fff;
    font-size: 16px;
    line-height: 40px;
    width: 40px;
    height: 40px;
    margin: 0 0 7px;
    border-radius: 50px;
    display: block;
    transition: all 0.3s ease 0s;
}
.product-grid .social li a:hover{ color: #6DA84A; }
.product-grid .product-rating{
    background: rgba(255,255,255,0.95);
    width: 100%;
    padding: 10px;
    opacity: 0;
    position: absolute;
    bottom: -60px;
    left: 0;
    transition: all .2s ease-in-out 0s;
}
.product-grid:hover .product-rating{
    opacity: 1;
    bottom: 0;
}
.product-grid .rating{
    padding: 0;
    margin: 0;
    list-style: none;
    float: left;
}
.product-grid .rating li{
    color: #6DA84A;
    font-size: 13px;
}
.product-grid .rating li.far{ color: #999; }
.product-grid .add-to-cart{
    color: #6DA84A;
    font-size: 14px;
    font-weight: 600;
    border-bottom: 1px solid #6DA84A;
    float:right;
    transition: all .2s ease-in-out 0s;
}
.product-grid .add-to-cart:hover{
    color: #000;
    border-color: #000;
}
.product-grid .product-content{
    background: #F5F5F5;
    padding: 15px;
}
.product-grid .title{
    font-size: 18px;
    text-transform: capitalize;
    margin: 0 0 5px;
}
.product-grid .title a{
    color: #111;
    transition: all 500ms;
}
.product-grid .title a:hover{ color: #6DA84A; }
.product-grid .price{
    color: #707070;
    font-size: 17px;
    text-decoration: underline;
}
.product-grid .price span{
    text-decoration: line-through;
    margin-right: 5px;
    display: inline-block;
    opacity: 0.6;
}
@media only screen and (max-width:990px){
    .product-grid{ margin-bottom: 40px; }
}
</style>
<template>
  <div class="container">
    <div class="row">
        <div class="col-md-3 col-sm-6">
            <div class="product-grid">
                <div class="product-image">
                    <a href="#" class="image">
                        <img class="pic-1" src="images/img-1.jpg">
                        <img class="pic-2" src="images/img-2.jpg">
                    </a>
                    <span class="product-sale-label"> Sale!</span>
                    <ul class="social">
                        <li><a href="" data-tip="Quick View"><i class="fa fa-search"></i></a></li>
                        <li><a href="" data-tip="Add to Wishlist"><i class="fa fa-heart"></i></a></li>
                        <li><a href="" data-tip="Compare"><i class="fa fa-random"></i></a></li>
                        <li><a href="" data-tip="Add to Cart"><i class="fa fa-shopping-cart"></i></a></li>
                    </ul>
                </div>
                <div class="product-content">
                    <h3 class="title"><a href="#">Men's Shirt</a></h3>
                    <div class="price"><span>$25.00</span> $21.00</div>
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
                        <li><a href="" data-tip="Quick View"><i class="fa fa-search"></i></a></li>
                        <li><a href="" data-tip="Add to Wishlist"><i class="fa fa-heart"></i></a></li>
                        <li><a href="" data-tip="Compare"><i class="fa fa-random"></i></a></li>
                        <li><a href="" data-tip="Add to Cart"><i class="fa fa-shopping-cart"></i></a></li>
                    </ul>
                </div>
                <div class="product-content">
                    <h3 class="title"><a href="#">Women's Fullsleve Top</a></h3>
                    <div class="price">$28.30</div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>
.product-grid{ font-family: "Poppins", sans-serif; }
.product-grid .product-image{
    overflow: hidden;
    position: relative;
    z-index: 1;
}
.product-grid .product-image a.image{ display: block; }
.product-grid .product-image a.image:before{
    content: "";
    background-color: rgba(24, 24, 24, 0.2);
    width: 100%;
    height: 100%;
    opacity: 0;
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;
    transition: all 250ms ease-out;
}
.product-grid:hover .product-image a.image:before{ opacity: 1; }
.product-grid .product-image img{
    width: 100%;
    height: auto;
}
.product-image .pic-1{
    opacity: 1;
    backface-visibility: hidden;
    transition: all 0.4s ease-in-out;
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
    transition: all 0.4s ease-in-out;
}
.product-grid:hover .product-image .pic-2{ opacity: 1; }
.product-grid .product-sale-label{
    color: #fff;
    background-color: #222;
    font-size: 11px;
    text-transform: uppercase;
    padding: 5px 10px 20px 45px;
    position: absolute;
    top: 0;
    right: 0;
    z-index: 1;
    transition: all 0.3s;
    -webkit-clip-path: polygon(100% 0, 0 0, 100% 100%);
    clip-path: polygon(100% 0, 0 0, 100% 100%);
}
.product-grid:hover .product-sale-label{ opacity: 0; }
.product-grid .social{
    text-align: center;
    width: 100%;
    padding: 0;
    margin: 0;
    list-style: none;
    transform: translateY(-50%);
    position: absolute;
    top: 50%;
    left: 0;
    z-index: 1;
}
.product-grid .social li{
    margin: 0 -12px 0 0;
    display: inline-block;
    opacity: 0;
    transform: translateX(70px);
    transition: all 0.4s;
}
.product-grid:hover .social li:nth-child(1){ transition-delay: 0s; }
.product-grid:hover .social li:nth-child(2){ transition-delay: 0.1s; }
.product-grid:hover .social li:nth-child(3){ transition-delay: 0.2s; }
.product-grid:hover .social li:nth-child(4){ transition-delay: 0.3s; }
.product-grid:hover .social li{
    margin: 0 2px;
    opacity: 1;
    transform: translateX(0);
}
.product-grid .social li a{
    color: #222;
    background: #fff;
    font-size: 16px;
    text-align: center;
    line-height: 45px;
    height: 45px;
    width: 45px;
    border-radius: 50px;
    display: block;
    transition: all 250ms ease-out;
}
.product-grid .social li a:hover{
    color: #fff;
    background: #3742fa;
}
.product-grid .social li a:before,
.product-grid .social li a:after{
    content: attr(data-tip);
    color: #fff;
    background-color: #222;
    font-size: 10px;
    line-height: 22px;
    padding: 2px 8px;
    white-space: nowrap;
    display: none;
    transform: translateX(-50%);
    position: absolute;
    left: 50%;
    top: -34px;
}
.product-grid .social li a:after{
    content: '';
    height: 15px;
    width: 15px;
    border-radius: 0;
    transform: translateX(-50%) rotate(45deg);
    top: -20px;
    z-index: -1;
}
.product-grid .social li a:hover:before,
.product-grid .social li a:hover:after{
    display: block;
}
.product-grid .product-content{
    text-align: center;
    padding: 20px 10px 10px;
}
.product-grid .title{
    font-size: 14px;
    font-weight: 400;
    text-transform: uppercase;
    margin: 0 0 7px;
}
.product-grid .title a{
    color: #222;
    transition: all 500ms;
}
.product-grid .title a:hover{ color: #3742fa; }
.product-grid .price{
    color: #222;
    font-size: 14px;
}
.product-grid .price span{
    margin-right: 3px;
    text-decoration: line-through;
}
@media only screen and (max-width:990px){
    .product-grid{ margin-bottom: 30px; }
}
</style>></style>
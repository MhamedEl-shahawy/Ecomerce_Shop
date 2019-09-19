<template>
  <div class="main">
  <div class="product">
          <div class="prev">
             <img :src="require(`@/assets/${placeholder}`)" />
          </div>
          <div class="info">
          <h3>Cristian Gilbanks</h3>
          <h4>$30.99</h4>
          <p>Etiam vel augue. Vestibulum rutrum rutrum neque. Aenean auctor gravida sem. Praesent id massa id nisl venenatis lacinia. Aenean sit amet justo. Morbi ut odio. Cras mi pede, malesuada in, imperdiet et, commodo vulputate, justo. In blandit ultrices enim. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</p>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto velit dolores repudiandae animi quidem, eveniet quod dolor facilis dicta eligendi ullam error. Assumenda in fugiat natus enim similique nam itaque.</p>
           <button @click="--val">-</button>
            <input type="number" :value="val">
           <button @click="++val">+</button>
           <p class="available">Available in additional colors: <span class="yellow">Yellow</span></p>
           <button class="cart">Add To Cart</button>
          </div>

  </div>
    <div class="reviews">
       <h3>Reviews</h3> 
       <p>ntegrate extensible methodologies</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum iusto placeat consequatur voluptas sit mollitia ratione autem, atque sequi odio laborum, recusandae quia distinctio voluptatibus sint, quae aliquid possimus exercitationem.</p>    
    </div>
    <section>
        <h2>
        <span>Featured Products</span>
        </h2> 
        <div class="featureditems">
        <div class="item">
        <img  src="../assets/1.jpg">
         <h3>Desi Avramovitz</h3>
          <h4>$50.40</h4>
           <router-link  to="/product/1.jpg"><a>
            <button class="multi-item">View Item &gt;</button>
            </a></router-link>
           </div>
           <div  class="item">
           <img  src="../assets/2.jpg"> 
           <h3 >Addy Alldre</h3> 
           <h4 >$33.99</h4>
            <router-link  to="/product/2.jpg"><a>
            <button class="multi-item">View Item &gt;</button>
            </a></router-link>
            </div>
            <div  class="item">
            <img  src="../assets/3.jpg"> 
            <h3>Bernie Gledhill</h3> 
            <h4>$102.99</h4> 
            <router-link  to="/product/3.jpg"><a>
            <button class="multi-item">View Item &gt;</button>
            </a></router-link>
            </div>
            </div>
            </section>
  </div>
</template>
<script>
// @ is an alias to /src

export default {
  name: 'men',
 data(){
    return{
      val:1,
      placeholder:this.$route.params.img,
    }
   },
   watch: {
          "$route.params.img"(val) {
           // call the method which loads your initial state
                   window.location.reload()
          },
       },
}
</script>
<style>
 .product{
    padding:3em;
    width:100%;
    display:grid;
    grid-template-columns: 1fr 2fr;
    grid-column-gap: 20px;
 }
 .product h3{
   font-size:2em;
   margin-bottom:2em;
 }
 .reviews p{
    font-family: "PT Serif",-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
    font-size:1.2em;
    color:#576574;
 }
 .product button{
 color:#fff;
 font-size:1.5em;
 padding:0.3em 0.8em;
  background-color:#111;
 }
 .product input{
       width: 60px;
    font-size: 25px;
    margin: 0 10px;
    padding: 5px 10px;
        font-family: Montserrat,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
        outline:none;
        border:1px solid #000;
 }
 .available{
  color:#576574;
 }
.yellow{
	 color:yellow;
	 font-size:1.3em;
	 font-weight:bolder;
}
.cart{
	 background: #d96528 !important;
    font-size: 20px !important;
    border: none;
     padding: 10px 14px;
    cursor: pointer;
    font-weight: 700;
}
.cart:hover{
border:none;
}

.reviews{
  margin-top:2em;	
}

.reviews h3{
	  font-size:1.7em;
}

@media screen and (max-width: 720px){
    .product{
      display:block;
      }
      .reviews{
       padding:1em;
      }
}
</style>
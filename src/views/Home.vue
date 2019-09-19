<template>
  <div class="home">
    <div class="textlockup">
      <div class="img">
      <img  src="../assets/shoe1.jpg" alt="shoe">
      </div>
     <div  class="new">New</div> 
     <div class="sale">Men Shoes</div> 
     <div class="collection">Collection</div>
      <div class="details">Street Style New Fashion</div>
      </div>
      <section  class="boxes">
      <div class="box0">
      <img  src="../assets/icon-package.svg" alt="service icon"> 
      <h4>Free Shipping Globally</h4>
       <p >Delivery in 4 Days</p>
       </div>
       <div  class="box1">
       <img  src="../assets/icon-cal.svg" alt="service icon"> 
       <h4 >24/7 Customer Service</h4>
        <p >Call us any time</p>
        </div>
        <div  class="box2">
        <img  src="../assets/icon-service.svg" alt="service icon"> 
        <h4>Easy Online Returns</h4> 
        <p >Send Within 30 Days</p>
        </div>
        </section>
        <div class="textlockup">
        <div class="img">
        <img  src="../assets/bag.jpg" alt="bag">
        </div>
         <div  class="new">50%</div> 
        <div  class="sale">Storewide Sale</div> 
        <div  class="collection">Summer</div> 
        <div  class="details">All accessories</div>
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
  name: 'home',
 
}
</script>
<style>
 .textlockup {
    display: grid;
    grid-template-columns: 50px 100px 1fr;
    grid-template-rows: 50px 50px 100px 20px 1fr;
    grid-column-gap: 0;
    grid-row-gap: 0;
}
.textlockup .img {
    max-width: 950px;
    grid-area: 1/3/6/4;
}
.textlockup .img img {
    width: 95%;
}
.textlockup .new{
    grid-area: 1/1/5/4;
    font-size: 23vmin;
    color: #efefef;
    text-transform: uppercase;
}
.textlockup .collection, .textlockup .sale,h3,h4,h2{
    font-family: "PT Serif",-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
}
.textlockup .sale {
 
        grid-area: 2/2/3/4;
    font-size: 4.5vmin;
    color: #d96528;

}

.textlockup .collection{
    grid-area: 3/3/4/4;
    font-size: 8.5vmin;
}
.textlockup .details{
    grid-area: 4/2/5/4;
    font-size: 2vmin;
    letter-spacing: .2em;
    text-transform: uppercase;
}
.boxes{
    margin: 70px 0;
}
.boxes div{
    border: 1px solid #ddd;
    min-height: 150px;
    justify-self: center;
    align-self: center;
    text-align: center;
        font-family: "PT Serif",-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;

}
h4{
    text-transform: uppercase;
    letter-spacing: .15em;
    margin: 0 0 10px;
}
p {
    margin: 20px 0;
}
.boxes .box1 {
    grid-area: 1/1/2/2;
}
.boxes .box2 {
    grid-area: 1/2/2/3;
}
h2 {
    text-align: center;
    overflow: hidden;
}
h2, h4 {
    color: #d96528;
}
h2 span{
    display: inline-block;
    position: relative;
    margin-top:2em;
}
h2 span:after, h2 span:before {
    content: " ";
    display: block;
    height: 1px;
    width: 1000px;
    background: #e6baa4;
    position: absolute;
    top: 50%;
}
h2 span:before {
    left: -1010px;
}
h2 span:after {
    right: -1010px;
}
.featureditems{
    width: 100%;
    margin: 20px 0 70px;
}
 button {
    -webkit-transition: all .3s ease;
    transition: all .3s ease;
    border: 1px solid #ccc;
    background: #fff;
    padding: 10px 14px;
    cursor: pointer;
    color: #000;
    font-weight: 700;
    font-family: Montserrat,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;

}
button:hover {
    background: #000;
    border: 1px solid #000;
    color: #fff;
}
a {
    color: #d96528;
    text-decoration: none;
        -webkit-transition: all .3s ease;

}
.featureditems .item {
    border: 1px solid #eee2dc;
    box-shadow: 0 3px 10px 0 #eee;
    border-radius: 40px;
    padding: 10px 20px 30px;
    min-height: 150px;
    justify-self: center;
    align-self: center;
    text-align: center;
}

@media screen and (min-width: 700px){
.boxes{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-column-gap: 20px;
    grid-row-gap: 0;
}
.boxes div{
    padding: 40px 50px;
}
.featureditems {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-column-gap: 20px;
    grid-row-gap: 0;
}
.featureditems img {
    max-width: 100%;
}
.featureditems div {
    padding: 40px 50px;
}
}
@media screen and (max-width: 699px){
 .boxes div{
      width:50vw;
  margin:auto;
  margin-top:2em;
  padding:1em;
 }
.featureditems {
    display: block;
    text-align:center;
}
.featureditems .item {
  width:50vw;
  margin:auto;
  margin-top:2em;
  padding:1em;
}
.featureditems img {
  margin:auto;
}
}
@media screen and (max-width: 500px){
.featureditems .item {
  width:70vw;
}
.textlockup .sale {
         font-size: 7vmin;
}
.textlockup .collection{
         font-size: 10vmin;     
}
.textlockup .details{
         font-size: 3.5vmin;     
}
}

</style>

<template>
  <div class="storegrid">
    <section  class="content">
        <div class="item" v-for="product in products">
            <img  :src="require(`@/assets/${product.img}`)"> 
            <h3>{{product.name}}</h3> 
            <h4>${{product.price}}</h4> 
            <router-link  :to="product.to"><a>
            <button class="multi-item">View Item &gt;</button>
            </a></router-link>
       </div>
        
        
     </section>
     <section class="range">
        <h3>Special Sale</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam libero iusto nemo laboriosam perferendis voluptas ullam officiis, quibusdam quas quam eveniet est fugit delectus corporis incidunt nam esse suscipit itaque?</p>
        <p><span>Filter by Price:</span><br>Max Price <span>${{this.val}}</span></p>
        <input  v-model="val" type="range" min="0" max="200" step="0.1" class="slider">
        <span  class="min">$0</span>
        <span  class="max">$200</span>
     </section>
  </div>
</template>
<script>
// @ is an alias to /src

export default {
  name: 'men',
  data(){
    return{
      val:40,
        products:[
        {
           name:"Bernie Gledhill",
           img:"4.jpg",
           to:"/product/4.jpg",
           price:80.55
        },
        {
           name:"Kalila Gooms",
           img:"6.png",
           to:"/product/6.png",
           price:30.99
        },
         {
           name:"Cristian Gilbanks",
           img:"7.png",
           to:"/product/7.png",
           price:80.50
        },
          {
           name:"Ardine Imlaw",
           img:"13.png",
           to:"/product/13.png",
           price:90.90
        },
        {

           name:"Bartolemo Peckitt",
           img:"8.png",
           to:"/product/8.png",
           price:20.78
        },
         {
           name:"Bernie Gledhill",
           img:"1.jpg",
           to:"/product/1.jpg",
           price:110.29
        },
         {
           name:"Armin Basilio",
           img:"11.png",
           to:"/product/11.png",
           price:103.00
        },
         {
           name:"Cal Sterman",
           img:"12.png",
           to:"/product/12.png",
           price:108.70
        },
      
        {
           name:"Gwendolen Bickerstaffe",
           img:"5.png",
           to:"/product/5.png",
           price:50.00
        }
        
      ]
    }
  }
 
}
</script>
<style>
.storegrid {
    width: 95%;
    display: grid;
    grid-template-columns: 3fr 1fr;
    grid-template-rows: 1fr;
    grid-column-gap: 40px;
    grid-row-gap: 0;
}
.content{
	 display:grid;
	 grid-template-columns:repeat(3,1fr);
    grid-column-gap: 10px;
    grid-row-gap: 10px;
}
.item{
	 text-align:center;
}
img{ 
  width:100%;
}
.range{
   margin-top:2em;
}
.range p{
   font-size:1.1em;
   color:#333;
       font-family: "PT Serif",-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;

}
p span{
   line-height:1.5em;
   font-weight:bolder;
   color:#000;
}
input[type=range].slider {
    -webkit-appearance: none;
    width: 100%;
    margin: 25px 0 5px;
    background:#d35400;
    height:10px;
    border-radius:10px;
        outline:none;

}
.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 22px;
  height: 22px;
  border-radius: 50%; 
  background: #fff;
  cursor: pointer;
  border:2px solid #e67e22;
}

.slider::-moz-range-thumb {
  appearance: none;
  width: 22px;
  height: 22px;
  border-radius: 50%; 
  background: #fff;
  cursor: pointer;
  border:2px solid #e67e22;
}
.max {
    display: inline-block;
    float: right;
}
@media screen  and (min-width: 520px) and (max-width: 720px){
  .storegrid {
     width: 100%;
    display: block;
  }

}
@media screen  and (max-width:519px){
  .storegrid {
     width: 100%;
    display: block;
  }
   .content{
      width: 100%;
    display: block;
   }
 
}
</style>
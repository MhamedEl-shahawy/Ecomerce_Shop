<template>
 <div>
  <div id="app">
  <header>
   <h1>Skyline Ivy</h1>
      <div class="head">
      <router-link to="/" tag="a">Home</router-link>
      <router-link to="/all" tag="a">all</router-link>
      <router-link to="/women" tag="a">women</router-link>
      <router-link to="/men" tag="a">men</router-link>
      <router-link to="/about" tag="a">cart</router-link>
      </div>
      </header>
    <router-view/>
  </div>
   <footer>
     <section class="callout">
     <h2>"The surprising styles of Skyline Ivy are advanced for all seasons."</h2>
      <p>Hansel Andersen</p>
      </section>
      <div class="mohamed">
      <p>
      This project is
      <a href="https://github.com/MhamedEl-shahawy/Ecomerce_shop">open source on github</a>,
      hosted with
      <a>Firebase</a>, and made with love by MohamedElshahawy,
      <a href="https://twitter.com/MohmedElshshawy">@MohmedElshshawy (twitter)</a> &amp;
      <a href="https://github.com/MhamedEl-shahawy" >@MhamedEl-shahawy (github)</a></p>
      </div>
    </footer>
  </div>

</template>

<style>
@import url('https://fonts.googleapis.com/css?family=PT+Serif&display=swap');
 *{
           box-sizing: border-box;
           margin: 0;
           padding: 0;
        }
       body{
         width:100%;
         border:9px solid #ccc;
         overflow-x:hidden; 
       }
#app{
   height:100%;
   padding:2em;
   padding-left:7em;
   padding-right:7em;

   overflow-x:hidden;
}
header{
   width:100%;
   text-align:center;
}
header h1{
   line-height:4em;
       font-family: "PT Serif",-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
       font-size:2.5em;
}
.head{
   width:100%;
   border-top:1px solid #ccc;
   border-bottom:1px solid #ccc;
   padding:0.7em;

}
.head a{
   text-decoration:none;
       border-left: 1px solid #ddd;
    border-right: 1px solid #ddd;
        text-transform: uppercase;
    letter-spacing: .1em;
    font-size: 13px;
    padding:0 20px;
    margin-left:0.8em;
    color:#000;
        font-family: Montserrat,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
}
.callout {
    width: 100%;
    height: 280px;
    background: url(assets/callout.jpg) 50% no-repeat;
    background-size: cover;
    display: -webkit-box;
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    color: #fff;
}
.mohamed {
    background: #000;
    width: 100%;
    padding: 10px 30px;
    color: #fff;
    text-align: center;
    font-family: Montserrat,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,sans-serif;
}
@media screen and (max-width: 850px){
#app{
   padding:1.5em;
}

}
@media screen and (max-width: 520px){
    #app{
      padding:0.5em;
      padding-right:0.9em;

    }
.head a{
    border:none;
    padding:0 3px;
  }
}

</style>

<template>
    <div>
        <!-- <section class="preloader">
          <div class="spinner">

               <span class="spinner-rotate"></span>
               
          </div>
     </section> -->


     <section class="navbar custom-navbar navbar-fixed-top" role="navigation">
          <b-container>

               <div class="navbar-header">
                    <button class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                         <span class="icon icon-bar"></span>
                         <span class="icon icon-bar"></span>
                         <span class="icon icon-bar"></span>
                    </button>

                    <a href="index.html" class="navbar-brand">Receitas</a>
               </div>

               <div class="collapse navbar-collapse">
                    <ul class="nav navbar-nav">
                         <li><a href="#home" class="smoothScroll">Pesquisa</a></li>
                         <li><a href="#about" class="smoothScroll">Sugestões</a></li>
                         <li><a href="#contact" class="smoothScroll">Contactos</a></li>
                    </ul>
                    <ul class="nav navbar-nav navbar-right">
                         <li><a href="#">Precisa de ajuda?- <span>receitas@gmail.com</span></a></li>
                    </ul>
               </div>

          </b-container>
     </section>

     <section id="home" data-stellar-background-ratio="0.5">
          <div class="overlay"></div>
          <b-container>
               <b-row>

                    <div class="d-flex justify-content-center w-100">   
                         <div class="home-info">                              
                              <h1>Procure as receitas que desejar!</h1>
                              <form  class="online-form">
                                   <input type="text" name="text" class="form-control" placeholder="Ingredientes..." v-model="pesquisa" required>
                                   <button type="button" class="form-control" @click="mostrar_receitas(pesquisa)">Procurar</button>
                              </form>
                         </div>
                    </div>

               </b-row>
          </b-container>
     </section>
<section>
  <b-container>
    <b-row>
      <div>
    <h4>Receitas encontradas:</h4>
    <b-row>
      
      <b-col cols="3" v-for= "(receita, index) in receitas" :key="index">
        <!-- <b-card  :img-src="receita.thumbnail" img-alt="Card image" img-bottom>
          <b-card-text>
            {{receita.title}}
          </b-card-text>
        </b-card> -->
       
          <b-card no-body>
            <b-card-body>
              <a :href="receita.href">
              <h4>{{receita.title}}</h4>
              <img :src="receita.thumbnail" alt="">
              </a>
              
            </b-card-body>
          </b-card>
        
      </b-col>
      
    </b-row>
    </div>
        <!-- <div v-for="(receita, index) in receitas" :key="index">
          <h3>{{receita.title}}</h3>
          <a :href="receita.href">
          <img :src="receita.thumbnail" alt="">
          </a>
      
        </div> -->
    </b-row>
  </b-container>
</section>

     <section id="about" data-stellar-background-ratio="0.5">
          <b-container>
               <b-row>

                    <b-col md="12" sm="12" class="col-md-offset-3">
                         <div class="section-title">
                              <h1>Sujestões</h1>
                         </div>
                    </b-col>

                    <b-col md="4" sm="4" >
                         <div class="team-thumb">
                              <a href="https://www.pingodoce.pt/receitas/costeletas-de-porco-com-couve-e-amendoa/" target="_blank"> 
                                <img src="../assets/images/costeletas-porco-couve-amendoa.png" class="img-responsive" alt="">
                                </a>
                              <div class="team-info team-thumb-up">
                                   <h2>Costeletas de porco com couve e amêndoa</h2>
                                   <small>30 minutos!/ 4 Pessoas</small>
                                   <p>Preparada com carne nacional, esta receita de costeletas de porco com couve e amêndoa é deliciosa e de confecção simples. Experimente e bom apetite!</p>
                              </div>
                         </div>
                    </b-col>

                    <b-col md="4" sm="4" >
                         <div class="team-thumb">
                              <div class="team-info team-thumb-down">
                                   <h2>Lombos de bacalhau no forno com legumes</h2>
                                   <small>50 minutos!/ 4 Pessoas</small>
                                   <p>Estes lombos de bacalhau no forno com legumes são um prato imprescindível à mesa dos portugueses. Acompanhe com salada e tomate cherry.</p>
                              </div>                     
                              <a href="https://www.pingodoce.pt/receitas/lombos-de-bacalhau-no-forno-com-legumes/" target="_blank"> 
                                <img src="../assets/images/lombos-de-bacalhau-com-legumes.jpg" class="img-responsive" alt="">
                                </a>
                         </div>
                    </b-col>

                    <b-col md="4" sm="4">
                         <div class="team-thumb">
                           <a href="https://www.pingodoce.pt/receitas/ravioli-salteados-com-espuma-de-alho-negro/" target="_blank"> 
                                <img src="../assets/images/ravioli-salteados-espuma-alho-negro.jpg" class="img-responsive" alt="">
                                </a>                            
                              <div class="team-info team-thumb-up">
                                   <h2>Ravioli salteados com espuma de alho negro</h2>
                                   <small>30 minutos!/ 4 Pessoas</small>
                                   <p>Se é fã de massas, vai adorar esta receita de ravioli salteados com espuma de alho negro. Um prato diferente que junta o sabor único da espuma de alho negro à versatilidade dos raviolis.</p>
                              </div>
                         </div>
                    </b-col>
                    
               </b-row>
          </b-container>
     </section>

     <section id="contact" data-stellar-background-ratio="0.5">
          <b-container>
               <b-row>

                    <b-col md="10" sm="12" class="col-md-offset-1">
                         <form id="contact-form" role="form" action="" method="post">
                              <div class="section-title">
                                   <h1>Envie a sua receita!</h1>
                              </div>
                              <b-row class="text-center">
                                 <b-col md="4" sm="4">
                                   <input type="text" class="form-control" placeholder="O seu nome" name="name" required>
                              </b-col>
                              <b-col md="4" sm="4">
                                   <input type="email" class="form-control" placeholder="Email" name="email" required>
                              </b-col>
                              <b-col md="4" sm="20">
                                   <input type="submit" class="form-control" name="send message" value="Enviar Receita" required>
                              </b-col>
                              <b-col md="12" sm="12">
                                   <textarea class="form-control" rows="8" placeholder="A sua receita" name="message" required></textarea>
                              </b-col>

                              </b-row>
                             
                         </form>
                    </b-col>

               </b-row>
          </b-container>
     </section>       


     <footer id="footer" data-stellar-background-ratio="0.5">
          <b-container>
               <b-row>

                    <div class="copyright-text col-md-12 col-sm-12">
                         <div class="col-md-6 col-sm-6">
                              <p>Copyright &copy;Luís Vieira</p>
                         </div>

                         <div class="col-md-6 col-sm-6">
                              <ul class="social-icon">
                                   <li><a href="#" class="fa fa-facebook-square" attr="facebook icon"></a></li>
                                   <li><a href="#" class="fa fa-twitter"></a></li>
                                   <li><a href="#" class="fa fa-instagram"></a></li>
                              </ul>
                         </div>
                    </div>

               </b-row>
          </b-container>
     </footer> 
      

    </div>
</template>

<script>
import axios from 'axios';
    export default {
      data() {
        return {
          receitas: [],
          pesquisa:''
        }
      },
      methods: {
        mostrar_receitas(pesq){
         axios
          .get('http://www.recipepuppy.com/api/?q='+pesq+'&p=3')
          .then(response => (this.receitas = response.data.results))
          .catch(err => console.log(err))
      } 
        }

        
    }
</script>

<style scoped>

  @import url('https://fonts.googleapis.com/css?family=Open+Sans:300,300i,400');

  body {
    font-family: 'Open Sans', sans-serif;
    overflow-x: hidden;
    background: #f9f9f9;
  }

  h1,h2,h3,h4,h5,h6 {
    font-weight: 300;
    line-height: normal;
  }

  h1 {
    font-size: 3em;
  }

  h2 {
    color: #353535;
    font-size: 2em;
  }

  p {
    color: #757575;
    font-size: 14px;
    font-weight: normal;
    line-height: 24px;
  }

  html{
    -webkit-font-smoothing: antialiased;
  }

  a {
    color: #202020;
    text-decoration: none !important;
  }

  a,
  input, button,
  .form-control {
    -webkit-transition: 0.5s;
    transition: 0.5s;
  }

  a:hover, a:active, a:focus {
    color: #29ca8e;
    outline: none;
  }

  ::-webkit-scrollbar{
    width: 8px;
    height: 8px;
  }

  ::-webkit-scrollbar-thumb {
    cursor: pointer;
    background: #202020;
  }

  .section-title {
    padding-bottom: 40px;
  }

  section {
    position: relative;
    padding: 100px 0;
  }

  #contact,
  footer {
    background: #ffffff;
    text-align: center;
  }

  .overlay {
    background: #536976; 
    background: -webkit-linear-gradient(to right, #292E49, #536976); 
    background: linear-gradient(to right, #292E49, #536976);
    opacity: 0.9;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .online-form {
    position: relative;
  }

  .online-form .form-control {
    border-color: #f0f0f0;
    display: inline-block;
    vertical-align: top;
    border-radius: 50px;
    box-shadow: none;
    height: 50px;
    margin-right: 0.5em;
    padding-left: 15px;
  }

  .online-form input[type="text"] {
    width: 60%;
  }

  .online-form button {
    background: #29ca8e;
    border: 0;
    color: #ffffff;
    position: absolute;
    right: 6em;
    width: 25%;
  }

  .online-form button:hover {
    background: #202020;
    color: #ffffff;
  }

  .section-btn {
    background: #29ca8e;
    border: 0;
    border-radius: 50px;
    color: #ffffff;
    font-size: 16px;
    font-weight: normal;
    padding: 12px 30px;
    transition: 0.5s 0.2s;
  }

  .section-btn:hover,
  .section-btn:focus {
    background: #202020;
    color: #ffffff;
  }

  .preloader {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 99999;
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    align-items: center;
    background: none repeat scroll 0 0 #ffffff;
  }

  .spinner {
    border: 1px solid transparent;
    border-radius: 3px;
    position: relative;
  }

  .spinner:before {
    content: '';
    box-sizing: border-box;
    position: absolute;
    top: 50%;
    left: 50%;
    width: 45px;
    height: 45px;
    margin-top: -10px;
    margin-left: -10px;
    border-radius: 50%;
    border: 1px solid #575757;
    border-top-color: #ffffff;
    animation: spinner .9s linear infinite;
  }



  @keyframes spinner {
    to {transform: rotate(360deg);}
  }


  .custom-navbar {
    border: none;
    margin-bottom: 0;
    padding: 25px 0;
  }

  .custom-navbar .navbar-brand {
    color: #ffffff;
    font-size: 25px;
    font-weight: 500;
    letter-spacing: -1px;
  }

  .top-nav-collapse {
    background: #ffffff;
  }

  .custom-navbar .navbar-nav {
    margin-left: 6em;
  }

  .custom-navbar .nav li a {
    font-size: 16px;
    font-weight: normal;
    color: #f0f0f0;
    padding-right: 22px;
    padding-left: 22px;
  }

  .custom-navbar .nav li a:hover {
    background: transparent;
    color: #29ca8e;
  }

  .custom-navbar .navbar-nav > li > a:hover,
  .custom-navbar .navbar-nav > li > a:focus {
    background-color: transparent;
  }

  .custom-navbar .nav li.active > a {
    background-color: transparent;
    color: #29ca8e;
  }

  .custom-navbar .navbar-toggle {
    border: none;
    padding-top: 10px;
  }

  .custom-navbar .navbar-toggle {
    background-color: transparent;
  }

  .custom-navbar .navbar-toggle .icon-bar {
    background: #29ca8e;
    border-color: transparent;
  }

  @media(min-width:768px) {
    .custom-navbar {
      border-bottom: 0;
      background: 0 0; 
    }

    .custom-navbar.top-nav-collapse {
      background: #ffffff;
      -webkit-box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      -moz-box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      padding: 10px 0;
    }

    .top-nav-collapse .navbar-brand {
      color: #252525;
    }

    .top-nav-collapse .nav li a {
      color: #575757;
    }

    .top-nav-collapse .nav .section-btn a {
      color: #ffffff;
    }
  }

  #home {
    background: url('../assets/images/Masterchef.jpg') no-repeat center center;
    background-size: cover;
    vertical-align: middle;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    min-height: 100vh;
    position: relative;
    padding-top: 12em;
    text-align: center;
  }

  #home h1 {
    color: #ffffff;
    margin-top: 10px;
    margin-bottom: 40px;
  }

  .home-info {
    margin-top: 7em;
  }

  .home-info h3 {
    color: #f0f0f0;
    font-size: 11px;
    font-weight: bold;
    letter-spacing: 4px;
    text-transform: uppercase;
    margin: 10px 0;
  }

  #about .col-md-4 {
    margin: 0;
    padding: 0;
  }

  .team-thumb {
    background: #ffffff;
    position: relative;
    overflow: hidden;
  }

  .team-thumb-up:after {
    display: block;
    margin: 0 auto;
    position: absolute;
    top: -15px;
    right: 0;
    left: 0;
    content: "";
    width: 0;
    height: 0;
    border-right: 15px solid transparent;
    border-left: 15px solid transparent;
    border-bottom: 15px solid #ffffff;
  }

  .team-thumb-down:after {
    display: block;
    margin: 0 auto;
    position: absolute;
    bottom: -15px;
    right: 0;
    left: 0;
    content: "";
    width: 0;
    height: 0;
    border-right: 15px solid transparent;
    border-left: 15px solid transparent;
    border-top: 15px solid #ffffff;
  }

  .team-info {
    position: relative;
    padding: 40px;
  }

  .team-info h2 {margin: 0;}

  .team-info small {
    display: block;
    font-size: 18px;
    margin: 5px 0 10px 0;
  }

  .team-thumb img {
    width: 100%;
  }

  #contact-form .col-md-12,
  #contact-form .col-md-4 {
    padding-left: 0;
  }

  #contact-form .form-control {
    background: transparent;
    border: 0;
    border-bottom: 3px solid #f0f0f0;
    border-radius: 0;
    box-shadow: none;
    margin: 10px 0;
  }

  #contact-form .form-control:focus {
    border-bottom-color: #202020;
  }

  #contact-form input {
    height: 50px;
  }

  #contact-form input[type='submit'] {
    background: #202020;
    border-radius: 50px;
    border: 0;
    color: #ffffff;
  }

  #contact-form input[type='submit']:hover {
    background: #29ca8e;
    color: #ffffff;
  }
 
  footer {
    padding-bottom: 80px;
  }

  .copyright-text p {
    margin: 5px;
  }

  .social-icon {
    position: relative;
    padding: 0;
    margin: 0;
  }

  .social-icon li {
    display: inline-block;
    list-style: none;
  }

  .social-icon li a {
    border-radius: 50px;
    color: #202020;
    font-size: 15px;
    width: 35px;
    height: 35px;
    line-height: 35px;
    text-decoration: none;
    text-align: center;
    position: relative;
    margin: 5px 5px 5px 0;
  }

  .social-icon li a:hover {
    background: #536976;
    color: #ffffff;
  }


  @media only screen and (max-width: 1200px) {

    .custom-navbar .navbar-nav {
      margin-left: 3em;
    }

    .home-info {
      margin-top: 0;
    }
  }


  @media only screen and (max-width: 992px) {

    section {
      padding: 60px 0;
    }

    .custom-navbar .navbar-nav {
      margin-left: 0;
    }

    .custom-navbar .nav li a {
      font-size: 14px;
      padding-right: 15px;
      padding-left: 15px;
    }

    #feature .nav-tabs>li>a {
      font-size: 16px;
      margin-right: 20px;
    }

    .feature-image {
      bottom: -24em;
    }

    .pricing-thumb {
      margin-bottom: 30px;
    }

    footer {
      padding-bottom: 40px;
    }
  }


  @media screen and (max-width: 767px) {

    .section-title {
      padding-bottom: 20px;
    }

    .custom-navbar {
      background: #ffffff;
      -webkit-box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      -moz-box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      box-shadow: 0 1px 30px rgba(0, 0, 0, 0.1);
      padding: 10px 0;
      text-align: center;
    }

    .custom-navbar .nav li a {
      line-height: normal;
      padding: 5px;
    }

    .custom-navbar .navbar-brand,
    .top-nav-collapse .navbar-brand {
      color: #202020;
      font-weight: normal;
    }

    .custom-navbar .nav li a,
    .top-nav-collapse .nav li a {
      color: #656565;
    }

    .feature-image {
      position: relative;
      bottom: 0;
    }

    #about .col-md-4:nth-child(3n) .team-thumb {
      display: flex;
      -webkit-box-orient: vertical;
      flex-direction: column-reverse;
      -webkit-flex-direction: column-reverse;
      -ms-flex-direction: column-reverse;
    }

    .team-thumb-down:after {
      top: -15px;
      bottom: inherit;
      border-top: inherit;
      border-bottom: 15px solid #ffffff;
    }

    .testimonial-image,
    .testimonial-info {
      height: 85vh;
    }

    .testimonial-info {
      padding: 30px;
    }
  }


  @media screen and (max-width: 480px) {

    .online-form input[type="email"],
    .online-form .form-control {
      width: 85%;
    }

    .online-form .form-control {
      display: block;
      margin: 20px auto;
    }

    .online-form button {
      position: relative;
      right: 0;
    }

    .testimonial-image,
    .testimonial-info {
      height: 65vh;
    }
  }

</style>
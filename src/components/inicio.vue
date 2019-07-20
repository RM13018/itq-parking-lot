<template>
  <div>
    <b-jumbotron style="background-color: #383635;" class="rounded-0 hd">
      <div class="container">
        <b-img :src="require('/home/beto/Documents/Soa/itq-parking-lot/src/assets/logoITQ2.png')" 
        fluid="Responsive Image" alt="ITQlogo" class="image1"></b-img> 
        <h1>TECNOLÓGICO NACIONAL DE MÉXICO</h1>
        <h2>INSTITUTO TECNOLÓGICO DE QUERÉTARO</h2>
      </div>
    </b-jumbotron>
    <b-container class="ctlnum">
      <b-form name="user">
        <b-row>
          <b-col></b-col>
          <b-col class="encabezado">Número de Control</b-col>
          <b-col></b-col>
        </b-row>
        <b-row>
          <b-col></b-col>
          <b-col class="in">
            <b-form-input id="entrada" v-model="ctlnm" 
            placeholder="Introduce tu número de control" @keypress.enter.prevent="cambiar(ctlnm,$event)">{{ctlnm}}
            </b-form-input>
          </b-col>
          <b-col></b-col>
        </b-row>
        <b-row>
          <b-col></b-col>
          <b-col class="botonIn">
            <b-button @click="cambiar(ctlnm,$event)" class="bn">Entrar</b-button>
          </b-col>
          <b-col></b-col>
        </b-row>
      </b-form>
    </b-container>
    <b-container class="passw">
      <b-form name="user">
        <b-row>
          <b-col></b-col>
          <b-col class="encabezado">Contraseña</b-col>
          <b-col></b-col>
        </b-row>
        <b-row>
          <b-col></b-col>
          <b-col class="in">
            <b-form-input id="entrada" v-model="pass" 
            placeholder="Introduce tu contraseña" type="password" :state="b" @keypress.enter.prevent="entrar(pass,$event)">{{pass}}
            </b-form-input>
          </b-col>
          <b-col></b-col>
        </b-row>
        <b-row>
          <b-col></b-col>
          <b-col class="botonIn">
            <b-button @click="entrar(pass,$event)" class="bn">Entrar</b-button>
          </b-col>
          <b-col></b-col>
        </b-row>
      </b-form>
    </b-container>
  </div>
</template>
<script>
export default {
  el: '#pasarApass',
  data:
    {
      ctlnm: '',
    },
  //metodos a definir
  methods:
  {
    hide: function()
    {
      document.getElementsByClassName('passw')[0].style.display='none'
    },
    cambiar: function(ctlnm,event)
    {
      if(event && ctlnm == '15140935')
      {
        document.getElementsByClassName('ctlnum')[0].style.display='none'
        document.getElementsByClassName('passw')[0].style.display='block'
      }
      else
      alert('Número de control incorrecto')
    },
    entrar: function(pass,event)
    {
      if(event && pass == '12345'){
      this.$router.push('/about')
      }
      else
      alert('contraseña no correcta!')
      
    }
  },
  mounted()
  {
    this.hide()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* 
{
  font-family: 'Nunito', sans-serif;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
h1 
{
  margin-top: 30px;
  font-size: 30px;
  color:white;
	font-weight: 400;
	font-variant:small-caps;
}
h2
{
  font-size: 25px;
	color:  #FF8C00;
	font-variant:small-caps;
}
.encabezado
{
  margin-top: 5px;
  background-color: #ec8013;
	color:#000;
	text-align:center;
	line-height:40px;
	font-variant:small-caps;
	font-size:20px;
	font-weight:200;
	border:1px solid transparent;
	border-radius:5px;
	padding:0px;
}
.in
{
  margin-top: 20px;
}
.form-control:focus {
  border-color: #ec8013;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(255, 0, 0, 0.6);
}
.botonIn
{
  margin-top: 50px;
}
.bn
{
transition: background 1s, color 1s;
	cursor: pointer;
	background: #ec8013;/*#ff6816;*/
	color:rgba(0,0,0,0.8);
	border:none;
	letter-spacing: 0.10em;

}
</style>

<template>
<!--<div>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    <v-container>
    <v-row align="center" justify="center">
      <v-col cols="auto">
        <v-btn density="compact" append-icon="mdi-vuetify size=">Button</v-btn>
        
      </v-col>
    </v-row>
  </v-container>

  </nav>
  <router-view/>
</div>  
-->
  
    <v-card>
      <v-layout>
        <!--<div style="display: flex;"> -->
          <v-navigation-drawer color="grey-darken-2" permanent :order="order" width="200"  >
            <v-list style="padding: 0px;">
              <v-list-item title="Barra Navegação" style="display: flex; justify-content: center ; padding-bottom: 75px">

                </v-list-item>

                  <v-list-item style="" v-for="(item, i) in menu_lateral" :key="i">
                        <div class="text-center">
                          
                              <v-menu :location="location">
                                <template v-slot:activator="{ props }">
                                  <v-btn 
                                    
                                    size="large"
                                    append-icon=""
                                    color="primary"
                                    dark
                                    v-bind="props"
                                    width="280"
                                    class=""
                                      > {{item.title}}
                                        <v-icon  icon="mdi-vuetify"></v-icon>
                                  </v-btn>
                                </template>

                            <v-list>
                              <v-list-item
                                v-for="(item, index) in items"
                                :key="index"
                                  >
                              <v-list-item-title>
                                <v-btn style="background-color: grey; color:antiquewhite">
                                 
                                  <router-link to="/Cadastrar_Cliente"> {{ item.title }}</router-link>
                                </v-btn>
                              </v-list-item-title>
                              
                              </v-list-item>
                            </v-list>
                          </v-menu>
                        </div>     
                </v-list-item>
                
            </v-list>
          </v-navigation-drawer>

          <v-app-bar height="100" color="grey-darken-2">
            <v-icon style="margin-left: 50px" icon="mdi-vuetify"></v-icon>
            <h1>BARBER SYSTEM</h1>
            <v-icon icon="mdi-vuetify"></v-icon>

          </v-app-bar>

          <router-view/> <!--Visualização dos componentes por meio das rotas-->

    
      </v-layout>
    </v-card>  
</template>

<script>
import itensLaterais from './components/itensLaterais.vue'

  export default {
    components: {
      itensLaterais
    },
    data: () => ({
      items: [
        { title: 'Cadastrar' },
        { title: 'Pesquisar' },
        { title: 'Editar' },
        { title: 'Excluir' },
      ],
      location: 'end',
      Modulos: [
        
      ],
      menu_lateral:[
        {title: 'Cliente'},
        {title: 'Funcionario'},
        {title: 'Servico'},
        {title:  'Agendamento'}
      ]
    }),
  }

</script>


<style scoped>
@media only screen and (min-width: 200px){
  .Content{
    background-color: aqua;
  }
}

.TopBar{
  height: 100px;
  display:flex;
  justify-content: center;
  align-items: center;
  background-color: gray;
  
  
}

.Content{
  background-color: black;
  opacity: 90%;
  background-image: url("./assets/BackGround.jpg");
  background-size: cover;
  margin-left: 180px;
}

/*
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
*/
</style>

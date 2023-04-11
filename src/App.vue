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
        <div style="display: flex;">
          <v-navigation-drawer color="grey-darken-2" permanent :order="order" width="200"  >
            <v-list style="padding: 0px;">
              <v-list-item title="Barra Navegação" style="display: flex; justify-content: center; padding-bottom: 75px">
                
              </v-list-item>
                <v-list-item style="">
                      <div class="text-center">
                        
                            <v-menu :location="location">
                              <template v-slot:activator="{ props }">
                                <v-btn 
                                  
                                  size="large"
                                  append-icon="mdi-account-circle"
                                  color="primary"
                                  dark
                                  v-bind="props"
                                  
                                    >
                                      Cliente
                                </v-btn>
                              </template>

                          <v-list>
                            <v-list-item
                              v-for="(item, index) in items"
                              :key="index"
                                >
                            <v-list-item-title>{{ item.title }}</v-list-item-title>
                            
                            </v-list-item>
                          </v-list>
                        </v-menu>
                      </div>     
              </v-list-item>
              
            </v-list>
          </v-navigation-drawer>

          <div style="margin-left: 200px; background-color: blanchedalmond; width: 1150px;" >
              <div  class="TopBar">
                    <v-icon  icon="mdi-vuetify"></v-icon>
                    <h1  >BARBER SYSTEM</h1>
                    <v-icon icon="mdi-vuetify"></v-icon>
              </div>

            <v-main style="min-height: 300px;height: 530px;" class="Content">

            </v-main>
          </div>
          
        </div>
      </v-layout>
    </v-card>
    <!--
    <div >
    </div>
    <div>
      <div elevation="1" height="100"  >
        
    </div>

    <v-main>
        <v-card height="530px"  >
          
        </v-card>
    </v-main>
    </div>
    -->
    
</template>

<script>
  export default {
    data: () => ({
      items: [
        { title: 'Cadastrar' },
        { title: 'Pesquisar' },
        { title: 'Editar' },
        { title: 'Excluir' },
      ],
      location: 'end',
      Modulos: [
        
      ]
    }),
  }

</script>


<style scoped>
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

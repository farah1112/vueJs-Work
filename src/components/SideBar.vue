<template>
<nav>
    <v-app-bar flat app color="white">
           <v-app-bar-nav-icon @click="drawer= true"></v-app-bar-nav-icon>
        <v-toolbar-title class="text-uppercase grey-text">
            <span class="font-weight-light" >CAT</span>
            <span right>CHIT</span>
               </v-toolbar-title> 
               <v-spacer></v-spacer>
             <v-text-field    prepend-icon="mdi-magnify"  ></v-text-field>
     

     
           
           
         
  
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer" temporary  color="white">
        <v-layout column align-center>
         <v-flex class="ml-15">
             <v-avatar size="150">
                 <img src="https://www.pngitem.com/pimgs/m/22-224065_avatar-people-icon-png-transparent-png.png" style="width:150px;height:150px">
             </v-avatar>
         </v-flex>
        </v-layout>
     
         <v-list color="black" >
      
      <v-list-item-group >
         
        <v-list-item v-for="item in items" :key="item.text" router :to="item.route" >
          <v-list-item-action>
            <v-icon style="     color:rgb(230, 230, 88)">{{item.icon}}</v-icon>
          </v-list-item-action>
          <br>
          <v-list-item-content>
            <v-list-item-title >{{item.text}}</v-list-item-title>
             
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    </v-navigation-drawer>
   
</nav>
</template>
<script>
export default {
    data() {
        return {
            drawer: false,
             items: [
        { text: 'Dashbord', icon: 'mdi-home ;' , route:'/DashbordView' },
        { text: 'Gestion User', icon: 'mdi-account' , route:'/GestionUser' },
            { text: 'Team', icon: 'mdi-account' , route:'/TeamView' },
            { text: 'Boutique', icon: 'mdi-shopping' , route:'/BoutiqueView' },
             { text: 'example', icon: 'mdi-shopping' , route:'/exampleView' },
               { text: 'login', icon: 'mdi-shopping' , route:'/loginView' },
        
      ],
        }
    },
}
</script>
<template>
<navbar-view/>
<v-divider></v-divider>
  <div>
    <v-row>
         <v-col
        cols="12"
        md="4"
      >
<v-col>
    <p class="font-weight-bold">
      Vos offres d'emploi
    </p>
        </v-col>
    <v-layout>
      <v-navigation-drawer
        floating
        permanent
      >
        <v-list
          density="compact"
          nav
        >
          <v-btn  flat rounded prepend-icon=" mdi-publish" title="  Publiez vos offres" value="  Publiez vos offres" to="PosteCompany" >Publiez vos offres</v-btn>
          <br><br>
          <v-btn   flat rounded prepend-icon="mdi-content-paste" title=" gérer vos offres" value=" gérer vos offres" to="GerePoste">gérer vos offres</v-btn>
          <br><br>
          <v-btn  flat rounded prepend-icon="mdi-forum" title="Statistiques" value="Statistiques" to="StatistCompany">Statistiques</v-btn>
          <br><br>
          <v-btn flat rounded prepend-icon="mdi-card-text-outline" title="Candidatures" value=" Candidatures" to="CandidatureCompany">Candidatures</v-btn>
            <br><br>
                  <v-col>
           <p class="font-weight-bold">
              Accès à la CVthèque
                </p>
                 </v-col>
            <v-btn  flat rounded prepend-icon="mdi-magnify" title=" Rechercher des CV's" value="Rechercher des CV's" to="RechercheCv">Rechercher des CV's</v-btn>
            <br><br>
          <v-btn  flat rounded prepend-icon=" mdi-briefcase-download-outline" title="CV's sauvgardés" value="CV's sauvgardés" to="SaveCv">CV's sauvgardés</v-btn>
          <br><br>
           <v-btn  flat rounded prepend-icon="mdi-bookmark-multiple-outline" title="Offres sauvgardés" value="Offres sauvgardés" to="OffreSave">Offres sauvgardés</v-btn>
        </v-list>
      </v-navigation-drawer>
      <v-main style="height: 750px"></v-main>
    </v-layout>
         </v-col>
    <v-col cols="12" md="8">
<v-icon size="40" color="green">mdi-bookmark-multiple-outline</v-icon>
<h5 class="font-weight-medium">Enregistrement des Offres Préférées</h5> 
<v-divider></v-divider>
<v-row>
  <v-col cols="12" md="12">
        <v-banner
    lines="Three"
    color="deep-purple-accent-4"
  >
    <v-banner-text>
        <v-row>
            <v-col cols="12" md="10">
        <router-link to="DetailsPost" style="text-decoration:none"><h5 class="font-italic">Développeur web Full Stack / Développeur web React</h5></router-link> 
        </v-col>
        </v-row>
         <v-icon color="yellow" size="30">mdi-flag-variant-outline</v-icon>
      <h6 class="font-weight-bold"> Tunis</h6>
      <p>On recrute un Développeur web Full Stack / Développeur web React.js - Français ...</p>
 </v-banner-text>
 <v-row>
     <v-col cols="12" md="8">
     </v-col>
         <v-col cols="12" md="4">
                    <v-tooltip
          v-model="show"
          top
        >
          <template v-slot:activator="{ props }">
            <v-btn
              icon
              v-bind="props"
            >
              <v-icon color="grey lighten-1">
                mdi-delete-empty
              </v-icon>
            </v-btn>
          </template>
          <span>Supprimer</span>
        </v-tooltip>
        </v-col>
 </v-row>
  </v-banner>
  </v-col>
</v-row>
<br><br>
      <div class="text-center">
    <v-btn
      color="green"
      rounded
      flat 
      @click="snackbar = true"
      prepend-icon="mdi-delete-empty"
    >
      Supprimer toute la liste
    </v-btn>

    <v-snackbar
      v-model="snackbar"
      vertical
    >
      <p>Vous etes sur de Supprimer ce contenu?</p>

      <template v-slot:actions>
        <v-btn
          color="indigo"
          variant="text"
          @click="snackbar = false"
        >
          Annuler
        </v-btn>
           <v-btn
          color="indigo"
          variant="text"
          @click="snackbar = false"
        >
        Supprimer
        </v-btn>
      </template>
    </v-snackbar>
  </div>
         </v-col>
         </v-row>
  </div>   
    <v-divider></v-divider>
    <footer-view/>
</template>
<script>
import NavbarView from '@/components/NavbarView.vue'
import FooterView from '@/components/FooterView.vue'
export default {
  components: { NavbarView, FooterView },
    data: () => ({
          snackbar: false,
      messages: [
        {
          avatar: 'https://cdn.icon-icons.com/icons2/1378/PNG/512/avatardefault_92824.png',
          name: 'Farah weslati',
          title: 'Vue js developer',
        },
      ],
      parag: 'je suis un developer vue js j ai 5 ans d expéerience .J ai un diplome en informatique.Je souhaite me spécialiser dans le domaine de Développement Web .Je suis assidue ,ambitieuse et Prête a mettre mes compétences et ma passion en pratique ',
      parag1:'Contact: Télephone:52214491 ',     
      parag2:'Email:farahweslati@gmail.com ',             
      parag3:'linkedin :https://www.linkedin.com/in/farah-weslati-52a5571bb/' 
     
    }),
}
</script>
<style>

</style>
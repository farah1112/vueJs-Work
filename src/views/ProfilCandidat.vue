<template>
<navbar-view/>
<v-divider></v-divider>
    <div>
        <v-container align="center">
            <h5>Mon compte</h5>
        </v-container>
             <v-container>
        <div align="center" style="border-style: ridge;" >
        <v-avatar size="100">
        <v-img src="https://toppng.com/uploads/preview/avatar-png-115540218987bthtxfhls.png" style=" width:100px;height:100px"></v-img>         
        </v-avatar>
        <v-col cols="auto">
      <v-dialog
        transition="dialog-top-transition"
      >
        <template v-slot:activator="{ props }">
         <v-btn flat rounded  v-bind="props"><v-icon>mdi-marker</v-icon></v-btn>
           </template>
        <template v-slot:default="{ isActive }">
          <v-card>
            <v-toolbar
              color="primary"
            >Télécharger votre photo</v-toolbar>
                   <v-icon style="margin-left:200px" size="50">
                  mdi-check-outline </v-icon>
            <v-card-text>
               <v-file-input
    :rules="rules"
    accept="image/png, image/jpeg, image/bmp"
    placeholder="Pick an avatar"
    prepend-icon="mdi-camera"
    label="Avatar"
    style="width:400px"
  ></v-file-input>
            </v-card-text>
            <v-card-actions class="justify-end">
             <v-btn
                text
                rounded
                @click="isActive.value = false"
              >Annuler</v-btn>
               <v-btn
                text
                rounded
                @click="isActive.value = false"
              >ENregistrer</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col>
        </div>
  </v-container>
  <v-container align="center">
      <v-row justify="center">
        <v-dialog
      v-model="dialog1"
      fullscreen
      :scrim="false"
      transition="dialog-bottom-transition"
    >
      <template v-slot:activator="{ props }">
   <v-btn flat rounded  v-bind="props"><v-icon>mdi-marker</v-icon></v-btn>
    </template>
      <v-card>
        <v-toolbar
          dark
          color="primary"
        >
          <v-btn
            icon
            dark
            @click="dialog1 = false"
          >
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Close</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
             <v-container fluid align="center">
         <h5 class="font-italic" style="color:cornflowerblue"><v-icon>mdi-account-group-outline</v-icon> Les Données personnelles</h5>
         <br>
 <v-row>
        <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            label="Nom de la société"
            prepend-inner-icon="mdi-bullhorn"
            placeholder="Placeholder"
            variant="outlined"
          ></v-text-field>
        </v-col>
        
        <v-col
          cols="12"
          sm="6"
        >
           <v-text-field
            label="ex:https://www.company.com"
            prepend-inner-icon="mdi-web"
            placeholder="Placeholder"
            variant="outlined"
          ></v-text-field>
        </v-col>
        </v-row>
        <v-row>
          <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            label="Le nombre des Employees "
            placeholder="Placeholder"
            variant="outlined"
             prepend-inner-icon="mdi-account"
          ></v-text-field>
          </v-col>
             <v-col
          cols="12"
          sm="6"
        >
         <v-text-field
            label="ex:1680 "
            placeholder="Placeholder"
            variant="outlined"
             prepend-inner-icon="mdi-account"
          ></v-text-field>
        </v-col>
        </v-row>
                <v-row>
          <v-col
          cols="12"
          sm="6"
        >
          <v-text-field
            label="Le Headquarts "
            placeholder="Placeholder"
            variant="outlined"
             prepend-inner-icon="mdi-garage"
          ></v-text-field>
          </v-col>
             <v-col
          cols="12"
          sm="6"
        >
         <v-text-field
            label="Location "
            placeholder="Placeholder"
            variant="outlined"
             prepend-inner-icon="mdi-map-marker"
          ></v-text-field>
        </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" md="2">
          <v-text-field
            color="success"
            label="LinkedIn"
          prepend-inner-icon="mdi-linkedin"
            placeholder="Placeholder"
            variant="outlined"
          ></v-text-field>
          </v-col>
              <v-col cols="12" md="2">
          <v-text-field
            color="success"
            label="Facebook"
           prepend-inner-icon="mdi-facebook"
            placeholder="Placeholder"
            variant="outlined"
          ></v-text-field>
        </v-col>
              <v-col cols="12" md="2">
          <v-text-field
            color="success"
            label="Twitter"
          prepend-inner-icon="mdi-twitter"
            placeholder="Placeholder"
            variant="outlined"
          ></v-text-field>
        </v-col>
          <v-col cols="12" md="6">
                 <v-textarea
        v-model="bio"
        auto-grow
        filled
        color="deep-purple"
        label="Description de la Société"
        rows="1"
      ></v-textarea>
          </v-col>
        </v-row>
          <v-row>
              <v-btn variant="outlined" color="blue" class="m-2" rounded flat  prepend-icon="mdi-floppy" style="padding-left:50px;padding-right:50px">Save </v-btn>
                <v-btn variant="outlined" color="red" class="m-2" rounded flat  prepend-icon="mdi-close-outline"  style="padding-left:50px;padding-right:50px">Annuler </v-btn>
              </v-row>
      </v-container>
      </v-card>
    </v-dialog>
    </v-row>
      <v-col>
         <h5>Informations professionnelles</h5>
             </v-col>
             <v-col>
                 <v-row justify="space-around">
    <v-col cols="auto">
      <v-dialog
        transition="dialog-bottom-transition"
      >
        <template v-slot:activator="{ props }">
        <v-btn flat rounded  v-bind="props"> <v-icon right size="20" >mdi-briefcase-edit-outline</v-icon> </v-btn>
        </template>
        <template v-slot:default="{ isActive }">
          <v-card>
            <v-toolbar
              color="primary"
            >Informations personnelles</v-toolbar>
               <v-icon style="margin-left:200px" size="50">
                  mdi-check-outline </v-icon>
            <v-card-text>
               <v-col
          cols="12"
          sm="12"
        >
          <v-text-field
            v-model="message4"
            label="Prénom"
            variant="outlined"
            clearable
            clear-icon="mdi-cancel"
            style="width:400px"
          ></v-text-field>
        </v-col>
         <v-col
          cols="12"
          sm="12"
        >
          <v-text-field
            v-model="message4"
            label="Nom"
            variant="outlined"
            clearable
            clear-icon="mdi-cancel"
             style="width:400px"
          ></v-text-field>
        </v-col>
            </v-card-text>
            <v-card-actions class="justify-end">
               <v-btn
                text
                rounded
                @click="isActive.value = false"
              >Annuler</v-btn>
               <v-btn
                text
                rounded
                @click="isActive.value = false"
              >ENregistrer</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col>
                 </v-row>
        </v-col>
         <h6>Weslati Farah</h6>
         <v-divider></v-divider>
        <v-col>
       <h5>Email</h5>
           </v-col>
           <v-col>
                 <v-row justify="space-around">
    <v-col cols="auto">
      <v-dialog
        transition="dialog-bottom-transition"
      >
        <template v-slot:activator="{ props }">
        <v-btn flat rounded  v-bind="props" > <v-icon right size="20"  v-bind="props" >mdi-briefcase-edit-outline</v-icon> </v-btn>
          </template>
        <template v-slot:default="{ isActive }">
          <v-card>
            <v-toolbar
               color="primary"
            >Changement de votre adresse email sur CATCH IT</v-toolbar>
                <v-icon style="margin-left:170px" size="50">
                  mdi-check-outline </v-icon>
            <v-card-text>
               <v-form>
    <v-container>
      <v-text-field>
        <template v-slot:label>
          What about <strong>anEmail</strong> here? <v-icon style="vertical-align: middle">
            mdi-file-find
          </v-icon>
        </template>
      </v-text-field>
    </v-container>
  </v-form>
   <v-form>
    <v-container>
      <v-text-field>
        <template v-slot:label>
          What about <strong>ConfirmEmail</strong> here? <v-icon style="vertical-align: middle">
            mdi-file-find
          </v-icon>
        </template>
      </v-text-field>
    </v-container>
  </v-form>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn
                text
                rounded
                @click="isActive.value = false"
              >Annuler</v-btn>
               <v-btn
                text
                rounded
                @click="isActive.value = false"
              >ENregistrer</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col>
                 </v-row>
        </v-col>
         <h6>farahwweslati1919@gmail.com</h6>
         <v-divider></v-divider>
         <v-col>
         <h5>Mot de passe </h5>
             </v-col>
             <v-col>
        <v-row justify="space-around">
    <v-col cols="auto">
      <v-dialog
        transition="dialog-bottom-transition"
      >
        <template v-slot:activator="{ props }">
        <v-btn flat rounded    v-bind="props" > <v-icon right size="20" >mdi-briefcase-edit-outline</v-icon> </v-btn>
         </template>
        <template v-slot:default="{ isActive }">
          <v-card>   
            <v-toolbar
                 color="primary"
            > Changer mot de passe </v-toolbar>
            <v-icon style="margin-left:200px" size="50">
                  mdi-check-outline </v-icon>
            <v-card-text>
                <v-col
          cols="12"
          sm="16"
        >
          <v-text-field
            v-model="password"
            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            :rules="[rules.required, rules.min]"
            :type="show1 ? 'text' : 'password'"
            name="input-10-1"
            label="Nouveau Password"
            hint="At least 8 characters"
            counter
            @click:append="show1 = !show1"
            style="width:400px"
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          sm="16"
        >
          <v-text-field
            v-model="password"
            :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            :rules="[rules.required, rules.min]"
            :type="show1 ? 'text' : 'password'"
            name="input-10-1"
            label="Confirmer Password"
            hint="At least 8 characters"
            counter
            @click:append="show1 = !show1"
            style="width:400px"
          ></v-text-field>
        </v-col>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn
                text
                rounded
                @click="isActive.value = false"
              >Annuler</v-btn>
               <v-btn
                text
                rounded
                @click="isActive.value = false"
              >ENregistrer</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-col>
                   </v-row>
             </v-col>
         <h6>* * * * * * * *</h6>
         <br>
         <br>
         <v-btn flat rounded color="blue" style="padding-left:80px; padding-right:80px">
             Se déconnecter
         </v-btn>
         <br>
         <br>
         <br>
           <v-row justify="center">
    <v-dialog
      v-model="dialog"
      persistent
    >
      <template v-slot:activator="{ props }">
          <v-hover><v-btn flat rounded  v-bind="props"  color="grey" style="padding-left:65px; padding-right:65px;">
             Supprimer ce Compte
         </v-btn>
          </v-hover>
          </template>
      <v-card>
        <v-card-title ><v-icon size="50">mdi-emoticon-cry-outline
          </v-icon>
        </v-card-title>
        <v-card-text>Êtes-vous certain de vouloir supprimer votre compte ?</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn 
         rounded
          flat
          style="background-color:green ;padding-left:40px;padding-right:50px"
            color="white"
            text
            @click="dialog = false"
          >
            Annuler
          </v-btn>
          <v-btn
          rounded
          flat
          style="background-color:grey ;padding-left:40px;padding-right:50px"
            color="white"
            text
            @click="dialog = false"
          >
          Delete
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
         </v-container>
         </div>
    <v-divider></v-divider>
    <footer-view/>
</template>




<script>
import NavbarView from '@/components/NavbarView.vue'
import FooterView from '@/components/FooterView.vue'
export default {
  components: { NavbarView, FooterView },
    data () {
      return {
         dialog1: false,
        notifications: false,
        sound: true,
        widgets: false,
        dialog: false,
         show1: false,
          message4: 'Hey!',
         password: 'Password',
        rules: {
          required: value => !!value || 'Required.',
          min: v => v.length >= 8 || 'Min 8 characters',
          emailMatch: () => (`The email and password you entered don't match`),
          
        },
        rules: [
        value => {
          return !value || !value.length || value[0].size < 2000000 || 'Avatar size should be less than 2 MB!'
        },
      ],
      }
    },
    
}
</script>

<style>
.dialog-bottom-transition-enter-active,
.dialog-bottom-transition-leave-active {
  transition: transform .2s ease-in-out;
}
</style>
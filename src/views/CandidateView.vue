<template>
<navbar-view/>
    <head>
	<link rel="stylesheet"
		href=
"https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
<v-container fluid style=" margin-top:50px">
<div>
	<center>
		<form style="max-width:450px;margin:auto">
			<h2>Join US</h2>
			<div class="input-icons">
				<i class="fa fa-user icon">
			</i>
				<input class="input-field"
					type="text"
					placeholder="FirstName">
			</div>
      <div class="input-icons">
				<i class="fa fa-user icon">
			</i>
				<input class="input-field"
					type="text"
					placeholder="LastName">
			</div>

			<div class="input-icons">
				<i class="fa fa-key icon">
			</i>
				<input class="input-field"
					type="password"
					placeholder="Password">
			</div>
        <div class="input-icons">
	
				<input class="input-field"
					type="text"
					placeholder="Position">
			</div>

            <v-spacer></v-spacer>
               <v-hover> <v-btn color="grey" rounded  flat block tile>Sign up</v-btn> </v-hover>
              <br>
              <p> Have an account! <router-link  to="/SignIn" style="color:green">SignIn</router-link> </p>
                <div align="center" justify="center" > 
                          <v-btn  style=" width:350px ; border-radius:30px" color="white " ><v-icon color="blue">mdi-facebook</v-icon> Facebook</v-btn> <br>
                          <br>
                           <v-btn  style=" width:350px ; border-radius:30px" color="white" ><v-icon color="red">mdi-google</v-icon> Google</v-btn> <br>
                           <br>
                             <v-btn  style="width:350px ; border-radius:30px" color="white" ><v-icon color="black">mdi-github</v-icon> Github</v-btn>
                     
                      </div>  
		</form>
	</center>
    </div>
    </v-container>
    <footer-view/>
</template>
<script>
import NavbarView from '@/components/NavbarView.vue'
import FooterView from '@/components/FooterView.vue'
export default {
  components: { NavbarView, FooterView },
    name:"SignIn"
}
</script>



<style>
        .input-icons i {
            position: absolute;
        }
        .input-icons {
            width: 100%;
            margin-bottom: 10px;
        }
          
        .icon {
            padding: 10px;
            color: green;
            min-width: 50px;
            text-align: center;
        }
          
        .input-field {
            width: 100%;
            padding: 10px;
            text-align: center;
        }
          
        h2 {
            color: green;
        }
</style>
<template>
	<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
		<div class="container-fluid">
			<a class="navbar-brand" href="#">Navbar</a>
		    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>
		    <div class="collapse navbar-collapse" id="navbarNavDropdown">
				<ul class="navbar-nav"	>
					<li class="nav-item">
						<a class="nav-link" v-bind:class="{'active':isActive1}" v-on:click="menu('Texto')">
							texto
						</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" v-bind:class="{'active':isActive2}" v-on:click="menu('Comments')" >
							formulario
						</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" v-bind:class="{'active':isActive3}" v-on:click="menu('menu3')">
							menu 3
						</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" v-bind:class="{'active':isActive4}" v-on:click="menu('menu4')" >
							menu 4
						</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>
</template>
<script>
	export default{
		data(){
			return{
				isActive1: true,
				isActive2: false,
				isActive3: false,
				isActive4: false
			}
		},
		methods:{
			menu(menu){
				this.isActive1 = menu === "Texto" ? true : false
				this.isActive2 = menu === "Comments" ? true : false
				this.isActive3 = menu === "menu3" ? true : false
				this.isActive4 = menu === "menu4" ? true : false
				this.$emit('pagina-menu',{
					link: menu
				})
			}
		}
	}
</script>
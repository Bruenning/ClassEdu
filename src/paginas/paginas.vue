<template>
	<div>
		<Comments v-if="metLinks() === 'Comments'"/>
		<Texto v-if="metLinks() === 'Texto'"/>
	</div>
</template>

<script>
import	Comments from '../components/Comments.vue'
import	Texto from '../components/quem-somos.vue'

export default{
	components:{
		Comments,
		Texto
	},
	props:{
		links: Object,
		default:String
	},
	methods:{
		log(...log){
			console.log(log);
		},
		metLinks(){
			return this.links.links ? this.links.links : this.links.default
		}
	}

}
</script>
<template>

  <article class="px-4 md:px-16 wrapper">
    <PortfolioTemplate :projectIndex="3" />

    
    <section class="my-8">
      <h2 class="text-white font-size-48 my-8 md:mt-16">
        Goal of project
      </h2>
      
      <p class="text-white md:w-2/3">
        After a couple of weeks learning HTML and CSS, I regularly struggled to remember CSS flexbox, which would frustrate me endlessly when buildings layouts. I decided that the best way to effectively learn flexbox was to build a project focused entirely on the given subject.
        <br>
        <br>
        I wanted a website that would display the most common flexbox properties, as well as the most common values for such properties. A text animation would cycle through these values, displaying an appropriate graphic to go alongside it. My goal was to regularly use the website for reference when building future projects, which I (and others) eventually did.
      </p>
      
      <h2 class="text-white font-size-48 my-8 md:mt-16 lg:mt-20">
        Challenges Faced
      </h2>
      
      <p class="text-white md:w-2/3">
        More than any previous client project, I managed to design a wireframe and hi-fi Figma prototype that was almost identical to the final product. Being a relatively simple project, there weren’t many technical hiccoughs. However, my problems came about when trying to deploy the website.
        <br>
        <br>
        Without the knowledge I have now of front-end website deployment services, such as Netlify and Vercel, my only obvious option at the time was to create a custom WordPress theme for CSS Display Info. Creating a WordPress theme took an unnecessary amount of time to learn and develop, though it gave me some beginner knowledge into PHP.
        <br>
        <br>
        This was also my first encounter with browser support issues. I learnt after publishing the website, through a comment on Reddit, that the websites UI had been terribly disfigured on Mozilla Firefox. I later found out that some of the methods of importing fonts, animations, and the blur property had differing levels of support to other browsers, such as Chrome and Opera. I later fixed these discrepancies when I moved from WordPress to Netlify.
      </p>
    </section>

    <section class="md:mt-16 md:grid md:grid-cols-2">
      <div class="md:mr-2">
        <h2 class="text-white font-size-48 my-8">
          Wireframes  
        </h2>
        <img :src="'/assets/images/portfolio/' + projectLink + '/showcase/wireframe/index.png'" :alt="'Wireframe of ' + projectName + ' website'" class="w-full">
      </div>
    
      <div class="md:ml-2">
        <h2 class="text-white font-size-48 my-8">
          Final Product
        </h2>
        <img :src="'/assets/images/portfolio/' + projectLink + '/showcase/final/index.png'" :alt="'Screenshot of ' + projectName + ' website'" class="w-full">
      </div>
    </section>

    <div class="flex justify-end w-full mt-8 md:mt-16">
      <a :href="project.websiteURL" :title="'website of ' + projectName" target="_blank">
        <button class="flex font-size-24 items-center mt-8 md:mt-0">
          View Live Site
          <div class="w-6 ml-4">
            <img src="/assets/images/icons/arrow.svg" alt="hand waving icon" class="w-full" />
          </div>
        </button>
      </a>
    </div>

  </article>
  
  

</template>


<script lang="ts">
import { Icon } from '@iconify/vue';
import PortfolioTemplate from './PortfolioTemplate.vue';
import portfolioItems from '../../data/portfolioItems.json'

export default {
  name: 'CSSDisplayInfo',
  components: {
		Icon,
    PortfolioTemplate,
	},
  // props: {

  // },
  data () {
    return {
      project: portfolioItems[3],
      projectName: 'CSS Display Info',
      projectLink: 'cssdisplayinfo',
    }
  },
  // methods: {

  // },
  // created () {

  // }
}

</script>


<style scoped lang="scss">
  @use '../../sass/abstracts' as *;
  @use '../../sass/themes' as *;



</style>
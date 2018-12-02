<template>
  <section class="container">
    <div class="content">
        <img src="../assets/profile_navy.jpg" style="width:80%; height:80%"  alt="trung nguyen in navy" />
        <div class="content-blog">
            <h2 class="title">Welcome to my blog</h2>
            <p>My name is Trung Nguyen. I'm a Full-Stack Software Engineer currently reside in Austin, TX. I work for a startup software company with a mission to help all people in need to find and connect with the social service programs they need (<a href="https://company.auntbertha.com/about/" target="_blank">https://company.auntbertha.com/about/</a>). I'm passionate about making reliable and useful software applications. I enjoy coding and learning new ideas.</p>

            <p>From being a first in my family to serve in the military (U.S Navy) to be the first to graduate college.  I now work as a full-time Software Engineer while continuing to contribute to the open-source projects and pursue my career in Data Science at Georgia Tech as an online graduate student. I build this blog to share my thought on the current trend of technology and also to showcase my hobby projects. Hope you will find this blog helpful and I'm also interested to hear what you think as well.</p>
        </div>

      <div class="links">
        <a
          v-for="link in links"
          v-bind:key="link.id"
          :href="`${link.url}`"
          :class="`${link.class}`"
          >
          {{ link.title }}
        </a>
      </div>
      <div class="social">
        <a
          v-for="social in socialLinks"
          v-bind:key="social.id"
          :href="`${social.url}`"
          target="_blank"
          >
          <img :src="`${social.image}`"  :alt="`${social.title }`" />
        </a>
      </div>
    </div>
    <no-ssr>
        <vue-particles
            color="#265e96"
            linesColor="#265e96"
            hoverMode="grab"
            :clickEffect="true"
            clickMode="push"
            :particleSize="5"
            :linesWidth="2"
            :particlesNumber="40"
        />
    </no-ssr>
  </section>
</template>

<script>
import ProfilePicture from '~/components/ProfilePicture.vue'

export default {
  components: {
    ProfilePicture
  },
  head () {
    return {
      title: 'Trung Nguyen - Full Stack Engineer, Data Science Apprentice',
      meta: [
        { hid: 'description', name: 'description', content: 'Code + Blog' },
        { property: 'twitter:card', content: 'summary' },
        { property: 'twitter:site', content: '@ntt2k' },
        { property: 'twitter:url', content: 'https://ntt2k.io/' },
        { property: 'og:description', content: 'From being a first in my family to serve in the military to be the first to graduate college. I now work as a Full-Stack Engineer while continuing to contribute to the Open-Source projects and pursue my career in Softwae Enginner / Data Science.' },
        { property: 'og:title', content: 'Trung Nguyen - Full Stack Engineer, Data Science Apprentice' },
        { property: 'og:image', content: 'https://ntt2k.io/profile.png' },
      ]
    }
  },
  data () {
    return {
      title: 'Trung Nguyen',
      links: [
        {
          id: 0,
          title: 'About',
          class: 'button--green',
          url: '/about'
        },
        {
          id: 1,
          title: 'Projects',
          class: 'button--blue',
          url: '/projects'
        },
        {
          id: 2,
          title: 'Coding Interview',
          class: 'button--grey',
          url: '/coding-interview'
        },
        {
          id: 3,
          title: 'Blog',
          class: 'button--green',
          url: '/blog'
        }
      ],
      socialLinks: [
        {
          id: 0,
          title: 'Twitter',
          image: require(`~/assets/twitter.svg`),
          url: 'https://twitter.com/ntt2k'
        },
        {
          id: 1,
          title: 'LinkedIn',
          image: require(`~/assets/linkedin.svg`),
          url: 'https://www.linkedin.com/in/ntt2k/'
        },
        {
          id: 3,
          title: 'GitHub',
          image: require(`~/assets/github.svg`),
          url: 'https://github.com/ntt2k'
        },
        {
          id: 4,
          title: 'GitLab',
          image: require(`~/assets/gitlab.png`),
          url: 'https://gitlab.com/ntt2k'
        },
        {
          id: 5,
          title: 'Medium',
          image: require(`~/assets/medium.png`),
          url: 'https://medium.com/@ntt2k'
        },
      ]
    }
  }
}
</script>

<style>
#particles-js {
  /* background-image: url('./assets/sky.jpg'); */
  /* background-size: cover; */
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.content {
    z-index: 100;
}

.content-blog {
    max-width: 800px;
}

.content-blog p {
    text-align: justify;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 54px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

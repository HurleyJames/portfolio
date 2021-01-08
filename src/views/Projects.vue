<template>
  <div class="container">
    <h1>Projects</h1>
    <p>Projects I participated in and/or developed.</p>

    <GitHubCard
      title="CodeHub"
      link="https://github.com/HurleyJames/CodeHub"
      :info="codehubInfo"
      :loading="loading"
    >
      <p>
        CodeHub是一款使用WanAndroid、Readhub以及Gank.io三者api开发的技术阅读类的开源项目。
        项目是基于Material Design + MVP + RxJava + Retrofit + Dagger2 + Glide等框架开发的。
      </p>
    </GitHubCard>

    <GitHubCard
      title="Social Proofs with Blockchain Consensus"
      link="https://github.com/epournaras/ProofOfSituationAwareness"
      :info="socialproofInfo"
      :loading="loading"
    >
      <p>
        This project is using blockchain smart contracts that prove social claims (situation awareness) on the smart phone.
      </p>
    </GitHubCard>

    <GitHubCard
      title="BioGA"
      link="https://github.com/HurleyJames/BioGA"
      :info="biogaInfo"
      :loading="loading"
    >
      <p>
        Biological and bio-inspired computation by genetic algorithm with BEAST.
      </p>
    </GitHubCard>

    <GitHubCard
      title="gatsby-starter-hurley"
      link="https://github.com/HurleyJames/gatsby-starter-hurley"
      :info="gatsbyhurleyInfo"
      :loading="loading"
    >
      <p>
        A blog template based on Gatsby.js and React.
      </p>
    </GitHubCard>

    <GitHubCard
      title="macOS-Big-Sur-icon-collection"
      link="https://github.com/HurleyJames/macOS-Big-Sur-icon-collection"
      :info="iconInfo"
      :loading="loading"
    >
      <p>
        macOS Big Sur style round corner icon collection.
      </p>
    </GitHubCard>

    <GitHubCard
      title="FootballLeague"
      link="https://github.com/HurleyJames/FootballLeague"
      :info="footballInfo"
      :loading="loading"
    >
      <p>Football league management system developed via Springboot + Thymeleaf + Layui...</p>
    </GitHubCard>

    <GitHubCard
      title="Computer-English-Words"
      link="https://github.com/HurleyJames/Computer-English-Words"
      :info="wordInfo"
      :loading="loading"
    >
      <p>
          English words of computer professional terms.
      </p>
    </GitHubCard>
  </div>
</template>

<script>
import GitHubCard from '@/components/GitHubCard.vue'

export default {
  components: {
    GitHubCard,
  },
  data() {
    return {
      loading: true,
      codehubInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      socialproofInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      biogaInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      gatsbyhurleyInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      footballInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
    }
  },
  mounted() {
    const githubApiUrl = 'https://api.github.com/repos'

    const codehubAxios = this.axios.get(`${githubApiUrl}/HurleyJames/CodeHub`)
    const socialproofAxios = this.axios.get(`${githubApiUrl}/epournaras/ProofOfSituationAwareness`)
    const biogaAxios = this.axios.get(`${githubApiUrl}/HurleyJames/BioGA`)
    const gatsbyhurleyAxios = this.axios.get(`${githubApiUrl}/HurleyJames/gatsby-starter-hurley`)
    const footballAxios = this.axios.get(`${githubApiUrl}/HurleyJames/FootballLeague`)

    this.axios
      .all([codehubAxios, socialproofAxios, biogaAxios, gatsbyhurleyAxios, footballAxios])
      .then(
        this.axios.spread((...resp) => {
          this.loading = false
          this.codehubInfo = resp[0].data
          this.socialproofInfo = resp[1].data
          this.biogaInfo = resp[2].data
          this.gatsbyhurleyInfo = resp[3].data
          this.footballInfo = resp[4].data
        }),
      )
      .catch(err => {
        this.loading = false
        // eslint-disable-next-line no-console
        console.error(err)
      })
  },
}
</script>

<style scoped>
.container .github-project-card:not(:last-child) {
  margin-bottom: 40px;
}

p {
  line-height: 30px;
}
</style>

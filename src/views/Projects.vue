<template>
  <div class="container">
    <h1>Projects</h1>
    <p>Projects I participated in and/or developed.</p>

    <GitHubCard title="CodeHub" link="https://github.com/HurleyJames/CodeHub" :info="codehubInfo" :loading="loading">
      <p>
        CodeHub 是一款使用 WanAndroid、Readhub 以及 Gank.io 三者 api 开发的技术阅读类的开源项目。 项目是基于 Material
        Design + MVP + RxJava + Retrofit + Dagger2 + Glide 等框架开发的。
      </p>
    </GitHubCard>

    <GitHubCard
      title="Social Proofs with Blockchain Consensus"
      link="https://github.com/epournaras/ProofOfSituationAwareness"
      :info="socialproofInfo"
      :loading="loading"
    >
      <p>
        This project is using blockchain smart contracts that prove social claims (situation awareness) on the smart
        phone.
      </p>
    </GitHubCard>

    <GitHubCard
      title="uol-covid19"
      link="https://github.com/HurleyJames/uol-covid19"
      :info="covid19Info"
      :loading="loading"
    >
      <p>
        Scrape the coronavirus case data from the University of Leeds website and generate the .csv files, make it as an
        Endpoint API Service.
      </p>
    </GitHubCard>

    <GitHubCard title="RTFSC-JDK" link="https://github.com/HurleyJames/RTFSC-JDK" :info="jdkInfo" :loading="loading">
      <p>Reading The Fucking Source Code - JDK</p>
    </GitHubCard>

    <GitHubCard
      title="interview-vuepress"
      link="https://github.com/HurleyJames/interview-vuepress"
      :info="interviewInfo"
      :loading="loading"
    >
      <p>Campus Recruitment Interview Experience.</p>
    </GitHubCard>

    <GitHubCard title="uScripts" link="https://github.com/HurleyJames/uScripts" :info="scriptInfo" :loading="loading">
      <p>Useful Scripts, involved Python, Shell, etc.</p>
    </GitHubCard>

    <GitHubCard
      title="macOS-Big-Sur-icon-collection"
      link="https://github.com/HurleyJames/macOS-Big-Sur-icon-collection"
      :info="iconInfo"
      :loading="loading"
    >
      <p>macOS Big Sur style round corner icon collection.</p>
    </GitHubCard>

    <GitHubCard
      title="NCHU_Bachelor_Thesis_Template"
      link="https://github.com/NCHUSC/NCHU_Bachelor_Thesis_Template"
      :info="nchuInfo"
      :loading="loading"
    >
      <p>A LaTeX template for bachelor thesis in Nanchang Hangkong University (NCHU).</p>
    </GitHubCard>

    <GitHubCard
      title="Computer-English-Words"
      link="https://github.com/HurleyJames/Computer-English-Words"
      :info="wordInfo"
      :loading="loading"
    >
      <p>English words of computer professional terms.</p>
    </GitHubCard>

    <GitHubCard
      title="AdvancedCalculator"
      link="https://github.com/HurleyJames/AdvancedCalculator"
      :info="calculatorInfo"
      :loading="loading"
    >
      <p>高级计算器，实现数字计算、汇率计算、亲戚关系三大功能。</p>
    </GitHubCard>

    <GitHubCard
      title="TrainSchedule"
      link="https://github.com/HurleyJames/TrainSchedule"
      :info="trainInfo"
      :loading="loading"
    >
      <p>火车时刻表是一款可以根据车站和车次来查询火车运行时刻表的安卓应用。</p>
    </GitHubCard>

    <GitHubCard
      title="FootballLeague"
      link="https://github.com/NCHUSC/FootballLeague"
      :info="footballInfo"
      :loading="loading"
    >
      <p>使用 Springboot + Thymeleaf + Layui + MySQL 开发的足球联赛管理系统。</p>
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
      covid19Info: {
        stargazers_count: 0,
        forks_count: 0,
      },
      jdkInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      interviewInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      scriptInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      iconInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      nchuInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      wordInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      calculatorInfo: {
        stargazers_count: 0,
        forks_count: 0,
      },
      trainInfo: {
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
    const covid19Axios = this.axios.get(`${githubApiUrl}/HurleyJames/uol-covid19`)
    const jdkAxios = this.axios.get(`${githubApiUrl}/HurleyJames/RTFSC-JDK`)
    const interviewAxios = this.axios.get(`${githubApiUrl}/HurleyJames/interview-vuepress`)
    const scriptAxios = this.axios.get(`${githubApiUrl}/HurleyJames/uScripts`)
    const iconAxios = this.axios.get(`${githubApiUrl}/HurleyJames/macOS-Big-Sur-icon-collection`)
    const nchuAxios = this.axios.get(`${githubApiUrl}/NCHUSC/NCHU_Bachelor_Thesis_Template`)
    const wordAxios = this.axios.get(`${githubApiUrl}/HurleyJames/Computer-English-Words`)
    const calculatorAxios = this.axios.get(`${githubApiUrl}/HurleyJames/AdvancedCalculator`)
    const trainAxios = this.axios.get(`${githubApiUrl}/HurleyJames/TrainSchedule`)
    const footballAxios = this.axios.get(`${githubApiUrl}/NCHUSC/FootballLeague`)

    this.axios
      .all([
        codehubAxios,
        socialproofAxios,
        covid19Axios,
        jdkAxios,
        interviewAxios,
        scriptAxios,
        iconAxios,
        nchuAxios,
        wordAxios,
        calculatorAxios,
        trainAxios,
        footballAxios,
      ])
      .then(
        this.axios.spread((...resp) => {
          this.loading = false
          this.codehubInfo = resp[0].data
          this.socialproofInfo = resp[1].data
          this.covid19Info = resp[2].data
          this.jdkInfo = resp[3].data
          this.interviewInfo = resp[4].data
          this.scriptInfo = resp[5].data
          this.iconInfo = resp[6].data
          this.nchuInfo = resp[7].data
          this.wordInfo = resp[8].data
          this.calculatorInfo = resp[9].data
          this.trainInfo = resp[10].data
          this.footballInfo = resp[11].data
        }),
      )
      .catch((err) => {
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

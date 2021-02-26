<template>
  <div class="container">
    <h1>Social</h1>
    <p>My followers of some social medias.</p>

    <div class="col-container">
      <div class="row-container">
        <statCard
          statTitle="Weibo"
          :followers="weibo.data"
          suffix="fans"
          icon="weibo.png"
          :loading="weibo.loading"
          link="https://weibo.com/5628559861"
        />
        <statCard
          statTitle="Zhihu"
          :followers="zhihu.data"
          suffix="followers"
          icon="zhihu.png"
          :loading="zhihu.loading"
          link="https://www.zhihu.com/people/huang-peng-yuan-91"
        />
      </div>
      <!-- <div class="row-container">
        <statCard
          statTitle="RSS"
          :followers="rss.data"
          suffix="subscribers"
          icon="rss.png"
          :loading="rss.loading"
          link="https://blog.spencerwoo.com/posts/index.xml"
        />
        <statCard
          statTitle="SSPAI"
          :followers="sspai.data"
          suffix="followers"
          icon="sspai.png"
          :loading="sspai.loading"
          link="https://sspai.com/u/spencerwoo/posts"
        />
      </div> -->
      <div class="row-container">
        <statCard
          statTitle="Jike"
          :followers="jike.data"
          suffix="likes"
          icon="jike.png"
          :loading="jike.loading"
          link="https://m.okjike.com/users/2C5A8DDF-8EB8-45FC-963C-7EE5C91DF570"
        />
        <statCard
          statTitle="GitHub"
          :followers="github.data"
          suffix="followers"
          icon="github.png"
          :loading="github.loading"
          link="https://github.com/HurleyJames"
        />
      </div>
      <div class="row-container">
        <statCard
          statTitle="NeteaseMusic"
          :followers="neteaseMusic.data"
          suffix="followers"
          icon="neteaseMusic.png"
          :loading="neteaseMusic.loading"
          link="https://music.163.com/#/user/home?id=310263001"
        />
        <statCard
          statTitle="Twitter"
          :followers="twitter.data"
          suffix="followers"
          icon="twitter.png"
          :loading="twitter.loading"
          link="https://twitter.com/HurleyHuang23"
        />
      </div>
      <div class="row-container">
        <statCard
          statTitle="Coolapk"
          :followers="coolapk.data"
          suffix="followers"
          icon="coolapk.png"
          :loading="coolapk.loading"
          link=""
        />
        <statCard
          statTitle="Instagram"
          :followers="instagram.data"
          suffix="followers"
          icon="instagram.png"
          :loading="instagram.loading"
          link="https://www.instagram.com/hurleyhuang/"
        />
      </div>
    </div>

    <p id="substats-footer">
      * Follower statistics powered by:
      <a href="https://api.spencerwoo.com/substats">Substats</a>.
    </p>
  </div>
</template>

<script>
import statCard from '@/components/StatCard.vue'

export default {
  components: {
    statCard,
  },
  data() {
    return {
      rss: { data: 0, loading: true },
      jike: { data: 0, loading: true },
      sspai: { data: 0, loading: true },
      zhihu: { data: 0, loading: true },
      weibo: { data: 0, loading: true },
      twitter: { data: 0, loading: true },
      neteaseMusic: { data: 0, loading: true },
      github: { data: 0, loading: true },
      coolapk: { data: 0, loading: true },
      instagram: { data: 0, loading: true },
    }
  },
  mounted() {
    const apiUrl = 'https://api.spencerwoo.com/substats'
    const rssUrl = 'https://blog.spencerwoo.com/posts/index.xml'

    const rssAxios = this.axios.get(`${apiUrl}/?source=feedly|inoreader&queryKey=${rssUrl}`)
    const sspaiAxios = this.axios.get(`${apiUrl}/?source=sspai&queryKey=spencerwoo`)
    const jikeAxios = this.axios.get(`${apiUrl}/?source=jikeLiked&queryKey=2C5A8DDF-8EB8-45FC-963C-7EE5C91DF570`)
    const zhihuAxios = this.axios.get(`${apiUrl}/?source=zhihu&queryKey=huang-peng-yuan-91`)
    const weiboAxios = this.axios.get(`${apiUrl}/?source=weibo&queryKey=5628559861`)
    const twitterAxios = this.axios.get(`${apiUrl}/?source=twitter&queryKey=HurleyHuang23`)
    const neteaseMusicAxios = this.axios.get(`${apiUrl}/?source=neteaseMusic&queryKey=310263001`)
    const githubAxios = this.axios.get(`${apiUrl}/?source=github&queryKey=HurleyJames`)
    const coolapkAxios = this.axios.get(`${apiUrl}/?source=coolapk&queryKey=795519`)
    const instagramAxios = this.axios.get(`${apiUrl}/?source=instagram&queryKey=hurleyhuang`)

    rssAxios.then((r) => {
      this.rss = { data: r.data.data.totalSubs, loading: false }
    })
    sspaiAxios.then((r) => {
      this.sspai = { data: r.data.data.totalSubs, loading: false }
    })
    jikeAxios.then((r) => {
      this.jike = { data: r.data.data.totalSubs, loading: false }
    })
    zhihuAxios.then((r) => {
      this.zhihu = { data: r.data.data.totalSubs, loading: false }
    })
    weiboAxios.then((r) => {
      this.weibo = { data: r.data.data.totalSubs, loading: false }
    })
    twitterAxios.then((r) => {
      this.twitter = { data: r.data.data.totalSubs, loading: false }
    })
    neteaseMusicAxios.then((r) => {
      this.neteaseMusic = { data: r.data.data.totalSubs, loading: false }
    })
    githubAxios.then((r) => {
      this.github = { data: r.data.data.totalSubs, loading: false }
    })
    coolapkAxios.then((r) => {
      this.coolapk = { data: r.data.data.totalSubs, loading: false }
    })
    instagramAxios.then((r) => {
      this.instagram = { data: r.data.data.totalSubs, loading: false }
    })
  },
}
</script>

<style lang="css" scoped>
.col-container {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: flex-start;
  align-items: stretch;
  align-content: center;
}

.row-container {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: stretch;
  align-content: stretch;
  margin: 15px 0px;
}

.row-container .statCard:last-child {
  margin-left: 30px;
}

.row-container .statCard {
  flex: 1;
}

@media screen and (max-width: 760px) {
  .row-container {
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: stretch;
    align-content: center;
  }

  .row-container .statCard:last-child {
    margin-left: 0px;
    margin-top: 30px;
  }
}

a {
  text-decoration: none;
}

p {
  line-height: 30px;
}

#substats-footer {
  color: #666666;
  text-align: left;
}
</style>

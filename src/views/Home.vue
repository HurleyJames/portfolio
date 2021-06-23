<template>
  <div class="container">
    <div id="name-container">
      <img id="avatar" src="./../assets/images/avatar.jpg" alt="avatar" />
      <h1>Hurley Huang</h1>
    </div>
    <div class="title-desc-container">
      <a id="github" href="https://github.com/HurleyWong"
        ><img class="title-font" src="./../assets/images/github.svg" />Github</a
      >
      <span>/</span>
      <a id="blog" href="https://blog.withh.life"
        ><img class="title-font" src="./../assets/images/blogger.svg" />Blog</a
      >
      <span>/</span>
      <a id="homepage" href="https://withh.life"
        ><img class="title-font" src="./../assets/images/homepage.svg" />Homepage</a
      >
      <span>/</span>
      <a id="soul" href="https://soul.withh.life"><img class="title-font" src="./../assets/images/soul.svg" />Soul</a>
      <span>/</span>
      <a id="notes" href="https://notes.withh.life"
        ><img class="title-font" src="./../assets/images/tech.svg" />Notes</a
      >
      <span>/</span>
      <a id="weibo" href="//weibo.com/5628559861" target="_"
        ><img class="title-font" src="./../assets/images/weibo.svg" />Weibo</a
      >
      <span>/</span>
      <a id="twitter" href="//twitter.com/HurleyHuang23" target="_"
        ><img class="title-font" src="./../assets/images/twitter.svg" />Twitter</a
      >
    </div>

    <div class="article">
      <h2>👨🏻‍💻 Name</h2>
      <p>Hey 👋 &nbsp; I'm Hurley Huang!</p>

      <h2>🛠 Programming</h2>
      <ul>
        <li>
          🎓 &nbsp;Fresh graduated master at 🇬🇧 &nbsp;<a href="https://www.leeds.ac.uk//">the University of Leeds</a>,
          <i
            >MSc in
            <a href="https://courses.leeds.ac.uk/i537/advanced-computer-science-artificial-intelligence-msc"
              >Advanced Computing Science (Artificial Intelligence)</a
            ></i
          >.
        </li>
        <li>🔭<b>&nbsp; Fields of interest:</b> 🤓 Mobile Dev / 😏 Front-end Dev / 🧐 Back-end Dev / 😅 ML.</li>
        <li>🎯<b>&nbsp; Target:</b> Full-Stack Engineer / Distributed Engineer / AI User</li>
      </ul>

      <h2>💻 Devices</h2>
      <ul>
        <li>MacBook Pro (13-inch, 2018) / Lenevo Xiaoxin Air 13 Pro</li>
        <li>iPad Air 3 / Apple Pencil</li>
        <li>iPhone 12 mini / iPhone 8 Plus / OnePlus 6T / Kindle</li>
        <li>AirPods Pro / BeatsX / Magic Trackpad 2</li>
      </ul>

      <h2>📥 Contacts</h2>
      <ul>
        <li>
          <b>📫&nbsp; Email me at: </b>
          <a href="hurleyhuang@outlook.com">hurleyhuang@hotmail.com</a><i> (Preferred)</i>
        </li>
        <li>
          <b>📨&nbsp; Contact me via: </b>
          <a href="https://withh.life/contact" target="_">Getform</a>
          in my Homepage
        </li>
        <li>
          <b>🇬🇧&nbsp; Catch me: </b>
          University of Leeds, Leeds, England
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="css" scoped>
#name-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
}

#avatar {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  margin-right: 12px;
}

#copyright:hover {
  border: none;
}

.title-font {
  width: 16px;
  height: 16px;
  margin-right: 4px;
}

.title-desc-container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin: 8px 0;
}

.title-desc-container a {
  display: flex;
  align-items: center;
}

.title-desc-container span {
  margin: 0px 4px;
}

.title-desc-container #github {
  color: #24292e;
}

.title-desc-container #blog {
  color: #d81e06;
}

.title-desc-container #portfolio {
  color: #b18a77;
}

.title-desc-container #tech {
  color: #1d96db;
}

a:hover {
  border-bottom: none;
}

h2 {
  font-size: 20px;
  padding: 16px 0 4px 0;
}

ul {
  padding-left: 15px;
  line-height: 30px;
  margin: 0;
}

p {
  line-height: 30px;
}
</style>

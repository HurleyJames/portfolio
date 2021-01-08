<template>
  <div class="container">
    <div id="name-container">
      <img id="avatar" src="./../assets/images/avatar.jpg" alt="avatar" />
      <h1>Hurley Huang</h1>
    </div>
    <div class="title-desc-container">
      <a id="github" href="https://github.com/HurleyJames"
        ><img class="title-font" src="./../assets/images/github.svg" />Developer</a
      >
      <span>/</span>
      <a id="blog" href="https://blog.hurley.fun"
        ><img class="title-font" src="./../assets/images/blogger.svg" />Blog</a
      >
      <span>/</span>
      <a id="portfolio" href="https://hurley.fun"
        ><img class="title-font" src="./../assets/images/portfolio.svg" />Portfolio</a
      >
      <span>/</span>
      <a id="tech" href="https://tech.hurley.fun"
        ><img class="title-font" src="./../assets/images/tech.svg" />Tech Site</a
      >
    </div>

    <div class="article">
      <h2>Name</h2>
      <p>
        Hey 👋 &nbsp; I'm Hurley Huang!
      </p>

      <h2>Academics</h2>
      <ul>
        <li>
          🎓 &nbsp;Fresh graduated master at 🇬🇧 &nbsp;<a href="https://www.leeds.ac.uk//">the University of Leeds</a>,
          <i>MSc in <a href="https://courses.leeds.ac.uk/i537/advanced-computer-science-artificial-intelligence-msc">Advanced Computing Science (Artificial Intelligence)</a></i>.
        </li>
        <li>🔭<b>&nbsp; Fields of interest:</b> Mobile Development / Front-end Development / Back-end Development.</li>
        <li>🎯<b>&nbsp; Target:</b> Full-Stack Engineer / Distributed Engineer / AI User</li>
      </ul>

      <h2>Devices</h2>
      <ul>
        <li>MacBook Pro (13-inch, 2018)</li>
        <li>iPad Air 3 / Apple Pencil</li>
        <li>iPhone 8 Plus / OnePlus 6T</li>
        <li>AirPods Pro / BeatsX / Magic Trackpad 2</li>
      </ul>

      <h2>Contacts</h2>
      <ul>
        <li>
          <b>📫&nbsp; Email me at: </b>
          <a href="hurleyhuang@outlook.com">hurleyhuang@outlook.com</a><i> (Preferred)</i>
        </li>
        <li>
            <b>📨&nbsp; Contract me via: </b>
            <a href="https://hurleyhuang.netlify.app/contact">Getform</a>
            of my blog
        </li>
        <li>
            <b>💬&nbsp; Ask me about anything </b><a href="https://github.com/HurleyJames/HurleyJames/issues">here</a>
        </li>
        <li>
            <b>🇬🇧&nbsp; Catch me: </b>
            University of Leeds, Leeds, UK
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

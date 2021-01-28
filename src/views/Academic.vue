<template>
  <div class="container">
    <h1>Academic</h1>
    <p>Welcome to Hurley's personal academic pages.</p>

    <div class="article">
      <h2>🙋‍♂️ Self-Intro</h2>
      <p>
        I show most interest in the field of <strong>Android</strong> development and even
        <strong>large front-end</strong> development. In terms of <strong>papers</strong>, I mainly focus on
        <strong>distributed systems</strong> and <strong>blockchain</strong>.
      </p>

      <h2>📒 Notes</h2>
      <ul>
        <li><a href="#" target="_">[[ Social Proofs with Blockchain Consensus ]]</a> - 基于区块链共识的社会证明</li>
        <li><a href="#" target="_">[[ Proof of Witness Presence ]]</a> - 基于区块链共识的存在证明</li>
        <li>
          <a href="#" target="_">[[ A Manifesto for Future Generation Cloud Computing ]]</a> -
          下一个十年的云计算研究方向
        </li>
        <li>
          <a href="#" target="_">[[ Calculating the BELU Score for Text in Python ]]</a> - Python 计算文本的 BLEU 分数
        </li>
      </ul>

      <h2>📝 Papers</h2>

      <h3>☁️ Distributed Systems</h3>
      <li>
        <a href="https://dl.acm.org/doi/abs/10.1145/3241737" target="_"
          >A Manifesto for Future Generation Cloud Computing: Research Directions for the Next Decade</a
        >
      </li>

      <h3>⛓ Blockchain</h3>
      <ul>
        <li>
          <a href="https://www.sciencedirect.com/science/article/abs/pii/S0743731520303282" target="_"
            >Proof of witness presence: Blockchain consensus for augmented democracy in smart cities</a
          >
        </li>
        <li><a href="https://link.springer.com/content/pdf/10.1007/s00607-019-00771-y.pdf" target="_">On cycling risk and discomfort: urban safety mapping and bike route recommendations</a></li>
      </ul>
    </div>
  </div>
</template>


<style lang="css" scoped>
a:hover {
  border-bottom: none;
  font-weight: bold;
}

h2 {
  font-size: 20px;
  padding: 16px 0 4px 0;
}

h3 {
  font-size: 16px;
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
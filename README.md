# Answers-to-Front-end-Developer-Interview-Questions
本文档是Github项目<a href="https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/Translations/Chinese/README.md#css-%E7%9B%B8%E5%85%B3%E9%97%AE%E9%A2%98">h5bp/Front-end-Developer-Interview-Questions</a>的部分答案。答案出处来自书籍或我自己的整理。
<ul >
  <li><a href="#htmlQuestions">HTML相关问题</a></li>
  <li><a href="#htmlAnswers">HTML相关问题答案</a></li>
</ul>

<h3 id="htmlQuestions">HTML相关问题</h3>
<ol type="1">
  <li>请解释 <code>&lt;script&gt;</code>、<code>&lt;script async&gt;</code> 和 <code>&lt;script defer&gt;</code> 的区别。</li>
  <li>为什么通常推荐将 CSS <code>&lt;link&gt;</code> 放置在 <code>&lt;head&gt;&lt;/head&gt;</code> 之间，而将 JS <code>&lt;script&gt;</code> 放置在 <code>&lt;/body&gt;</code> 之前？你知道有哪些例外吗？</li>
  <li>doctype(文档类型) 的作用是什么？</li>
</ol>

<h3 id="htmlAnswers">HTML相关问题答案&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#htmlQuestions">问题</a></h3>
<ol type="1">
  <li>
    <code>&lt;script&gt;</code>标签中可以包含内部代码，或外部脚本文件。在解释器对<code>&lt;script&gt;</code>中的所有代码解析完毕之前，页面中的其他内容都不会被浏览器加载或显示。
          <code>&lt;script async&gt;</code>是<code>&lt;script&gt;</code>的一个可选属性，这个属性只对外部脚本文件有效。它允许立即下载该标签中的脚本，但不应妨碍页面中的其他操作。
          <code>&lt;script defer&gt;</code>同样是<code>&lt;script&gt;</code>的一个可选属性，这个属性只对外部脚本文件有效。它表示脚本可以延迟到文档完全被解析和显示之后再执行。
          只要不存在defer和async属性，浏览器都会按照<code>&lt;script&gt;</code>元素在页面中出现的先后顺序对它们依次进行解析。
  </li>
  <li>
      在文档的 <code>&lt;head&gt;&lt;/head&gt;</code> 中包含所有的JS文件，意味着必须等所有的JS代码被下载、解析、执行后才加载页面内容。对于需要很多JS代码的页面来说，会导致浏览器在呈现页面时出现明显的延迟，延迟期间浏览器窗口空白。
  </li>
  <li>
        IE5.5引入了文档模式的概念，而这个概念是通过使用文档类型 (doctype) 切换实现的。如果在文档开始处没有声明文档类型，所有浏览器会默认开启混杂模式。而不同浏览器在这种模式下的行为差异非常大，如果不采用某些hack技术，跨浏览器的行为根本没有一致性可言。
  </li>
</ol>

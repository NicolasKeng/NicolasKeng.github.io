---
layout: home-profile
permalink: /
title: "Nicolas Keng’s Homepage in Chinese"
excerpt: "Graduate student in pure mathematics at Shandong University. Writings, seminars, talks, and open study materials in number theory and beyond."
author_profile: false
redirect_from:
  - /about.html
  - /about/
---

<header class="nk-intro nk-intro--chinese" aria-labelledby="home-title">
  <div class="nk-intro__summary" data-balanced-intro>
    <div class="nk-intro__hero">
      <div class="nk-intro__heading">
        <h1 id="home-title">Nicolas Keng’s Homepage in Chinese</h1>
        <p class="nk-intro__lead"><a href="{{ '/en/' | relative_url }}">Homepage in English HERE</a></p>
      </div>
      <div class="nk-note">
        <p>
          我是山大青岛数学与交叉科学研究中心 2025 级基础数学研究生 耿浩源.<br>
          我之前在山大数学学院读本科, 2025 年毕业, 其中, 我在第四学年在中科院交流.<br>
          我关注算术几何, 数论及相关方向, 尤其是 Iwasawa 理论, BSD 猜想等.<br>
          我在这里记录我的数学学习过程, 保存讨论班讲义和开放给后来者使用的学习资料. 我也会时常在此分享自己的一些非数学的兴趣内容. 你可以在<a href="#contact-title">这里</a>联系我.
        </p>
      </div>
    </div>
    <figure class="nk-intro__portrait">
      <img src="{{ '/images/luotianyi-heart.jpg' | relative_url }}" alt="洛天依比心" width="1024" height="1024">
    </figure>
  </div>

  <dl class="nk-details">
    <div><dt>Affiliation</dt><dd><a href="https://www.math.sdu.edu.cn/">Shandong University</a></dd></div>
    <div><dt>Advisor</dt><dd><a href="http://www.prime.sdu.edu.cn/info/1023/1773.htm">Prof. Shuai Zhai</a></dd></div>
    <div><dt>Location</dt><dd>Qingdao, China</dd></div>
  </dl>
</header>

<section class="nk-home-section nk-interests" aria-labelledby="interests-title">
  <h2 id="interests-title">兴趣方向</h2>
  <p>我主要对数论与算术几何感兴趣, 尤其关注 Iwasawa 理论相关的内容. 具体包括: </p>
  <ul>
    <li>Iwasawa 理论的算术应用, 比如 BSD 猜想等; </li>
    <li>Heegner 点及其在 $L$ 函数特殊值与二次扭族中的应用, 也涵盖相关的反分圆主猜想. </li>
  </ul>
  <p>我也对很多其他非数学的内容感兴趣, 具体包括: </p>
  <ul>
    <li>书法; </li>
    <li>汉语言文字学; </li>
    <li>VOCALOID, 尤其是洛天依 (你可以在我的主页元素中很明显地看出来这一点). </li>
  </ul>
</section>

<section class="nk-home-section" aria-labelledby="recent-title">
  <h2 id="recent-title">最近动态</h2>
  {% assign recent_lectures = site.lectures | where_exp: "item", "item.pinned != true" %}
  {% assign recent_notes = site.learnings | where_exp: "item", "item.pinned != true" %}
  {% assign recent_updates = recent_lectures | concat: recent_notes | sort: "date" | reverse %}
  <div class="nk-reading-list" data-recent-updates>
    {% for item in recent_updates limit: 2 %}
    <a href="{{ item.url | relative_url }}">
      <span>{% if item.collection == "lectures" %}LECTURE{% else %}NOTE{% endif %}</span>
      <span class="nk-reading-list__content">
        <strong>{{ item.title }}</strong>
        <small>{{ item.excerpt | strip_html | strip_newlines }}</small>
      </span>
    </a>
    {% endfor %}
    <a href="{{ '/miscellanies/SDUMath-Exams' | relative_url }}">
      <span>ARCHIVE</span>
      <span class="nk-reading-list__content">
        <strong>SDU Math Archive</strong>
        <small>持续整理的山东大学数学课程, 历年试题与学习资料. </small>
      </span>
    </a>
  </div>
  <aside class="nk-update-note">
    <strong>转载与勘误</strong>
    <p>请勿使用这里的个人内容牟利. 如果发现笔记中的错误或任何不妥, 欢迎随时告诉我. </p>
  </aside>
</section>

<section class="nk-home-section nk-purpose-link" aria-labelledby="why-share-title">
  <h2 id="why-share-title"><a href="{{ '/miscellanies/before/' | relative_url }}">关于网站设立的初衷</a></h2>
  <p>数学学习最需要的是环境与眼界. 我希望这些并不完美的资料, 能让更多人更早感受到数学的美好.</p>
</section>

<section class="nk-home-section nk-home-section--contact" aria-labelledby="contact-title">
  <h2 id="contact-title">联系方式</h2>
  <div class="nk-contact-directory">
    <a href="mailto:nicolaskeng2004@163.com">
      <span>Mathematics</span>
      <strong>nicolaskeng2004@163.com</strong>
      <small>数学交流与笔记勘误</small>
    </a>
    <a href="mailto:knk2004@163.com">
      <span>Elsewhere</span>
      <strong>knk2004@163.com</strong>
      <small>数学之外的邮件</small>
    </a>
    <div>
      <span>QQ &amp; WeChat</span>
      <strong>3036536992</strong>
      <small>添加时请备注学校, 学院与姓名</small>
    </div>
    <a href="https://www.zhihu.com/people/nicolas-keng">
      <span>Zhihu</span>
      <strong>@Nicolas Keng</strong>
      <small>习题答案与相关更新</small>
    </a>
  </div>
</section>

<script>
  (() => {
    const intro = document.querySelector(".nk-intro--chinese");
    const summary = document.querySelector("[data-balanced-intro]");
    const siteContent = document.querySelector(".nk-site-content");
    const home = document.querySelector(".nk-home");
    if (!intro || !summary || !siteContent || !home) return;

    const desktop = window.matchMedia("(min-width: 1121px)");
    let frame = 0;

    const clamp = (value, minimum, maximum) => Math.min(Math.max(value, minimum), maximum);

    const balanceIntro = () => {
      cancelAnimationFrame(frame);
      frame = requestAnimationFrame(() => {
        if (!desktop.matches) {
          intro.style.removeProperty("--nk-intro-portrait-size");
          intro.style.removeProperty("--nk-intro-summary-width");
          intro.style.removeProperty("--nk-intro-text-width");
          intro.style.removeProperty("--nk-intro-full-width");
          return;
        }

        const contentBounds = siteContent.getBoundingClientRect();
        const homeBounds = home.getBoundingClientRect();
        const summaryLeft = summary.getBoundingClientRect().left;
        const textWidth = Math.max(0, homeBounds.right - summaryLeft);
        const portraitSize = contentBounds.width / 6;
        const gap = clamp(contentBounds.width * 0.018, 20, 36);
        const summaryWidth = textWidth + gap + portraitSize;
        const fullWidth = Math.max(0, contentBounds.right - summaryLeft);

        intro.style.setProperty("--nk-intro-summary-width", `${Math.round(summaryWidth * 10) / 10}px`);
        intro.style.setProperty("--nk-intro-text-width", `${Math.round(textWidth * 10) / 10}px`);
        intro.style.setProperty("--nk-intro-portrait-size", `${Math.round(portraitSize * 10) / 10}px`);
        intro.style.setProperty("--nk-intro-full-width", `${Math.round(fullWidth * 10) / 10}px`);
      });
    };

    window.addEventListener("resize", balanceIntro, { passive: true });
    desktop.addEventListener?.("change", balanceIntro);
    document.fonts?.ready.then(balanceIntro);
    balanceIntro();
  })();
</script>

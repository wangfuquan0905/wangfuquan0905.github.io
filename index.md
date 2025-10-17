---
layout: about
title: "About Me"
permalink: /
image: /assets/img/blog/bg.jpg
hide_description: true
---

<!--author-->

{% include news.html %}
---

## Publications {#publications}

{% assign items = site.projects | sort: "year" | reverse %}
{% if items and items.size > 0 %}
  <div class="pub-list" style="margin-top:1.5rem;">
    {% for p in items %}
      <a href="{{ p.link | default: p.url | relative_url }}" target="_blank" style="text-decoration:none; color:inherit;">
        <div class="pub-item" style="display:flex; align-items:flex-start; margin-bottom:1.5rem; gap:1rem; border-radius:10px; padding:0.75rem; transition:all 0.2s ease;">
          {% if p.image %}
            <div class="pub-thumb" style="flex:0 0 200px;">
              <img src="{{ p.image | relative_url }}" alt="{{ p.title }}" style="width:100%; border-radius:8px;">
            </div>
          {% endif %}

          <div class="pub-meta" style="flex:1;">
            <p style="margin:0; font-weight:600;">{{ p.title }}</p>
            <p class="pub-authors" style="margin:0.25rem 0; line-height:1.4;">
              {{ p.authors | replace: "Fuquan Wang", "<strong>Fuquan Wang</strong>" }}
            </p>
            <p class="pub-venue">
              {{ p.venue }}{% if p.year %}, {{ p.year }}{% endif %}
            </p>
          </div>
        </div>
      </a>
    {% endfor %}
  </div>
{% else %}
  <p style="color:#888;">(No publications yet)</p>
{% endif %}

---
## 🤖 Robots I Worked With {#robots}

<div class="robot-grid">

  <!-- 左列：竖着的 TIAGo（占两行） -->
  <a class="robot-card tall" href="https://pal-robotics.com/robot/tiago/" target="_blank">
    <div class="robot-media">
      <img src="/assets/img/robots/tiago.png" alt="PAL Robotics TIAGo" loading="lazy">
    </div>
    <span>PAL Robotics TIAGo</span>
  </a>

  <!-- 右上：Realman -->
  <a class="robot-card" href="https://www.realman-robotics.com/rm-series123" target="_blank">
    <div class="robot-media">
      <img src="/assets/img/robots/realman.png" alt="Realman RM Series" loading="lazy">
    </div>
    <span>Realman RM Series</span>
  </a>

  <!-- 右下：Rizon（补在 Realman 下） -->
  <a class="robot-card" href="https://www.flexiv.com/products/rizon" target="_blank">
    <div class="robot-media">
      <img src="/assets/img/robots/rizon.png" alt="Flexiv Rizon" loading="lazy">
    </div>
    <span>Flexiv Rizon</span>
  </a>

</div>

---


<section id="visitors-globe" style="margin-top:2rem">
  <div style="display:flex;justify-content:center;align-items:center;
              border-radius:12px;padding:1rem;">
    <!-- 控制球体大小 -->
    <div style="width:300px;height:300px;max-width:90vw;">
      <script type="text/javascript" id="mmvst_globe"
        src="//mapmyvisitors.com/globe.js?d=Z5y04Z-eCtGSfnuvFDB4y5gRbyxMvXy2thDsh94gnI">
      </script>
    </div>
  </div>
</section>


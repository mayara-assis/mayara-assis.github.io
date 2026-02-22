---
layout: default
title: Blog
---

Bem-vindo ao meu espaço de reflexões e artigos. Aqui compartilho percepções da prática clínica fonoaudiológica, bastidores de pesquisa na aquisição da linguagem e dicas sobre desenvolvimento da comunicação humana.

<div class="blog-grid" style="display: grid; grid-template-columns: 1fr; gap: 2rem; margin-top: 3rem;">
  {% for post in site.posts %}
    <article class="post-card" style="background: var(--color-surface); border: 1px solid var(--color-border); border-radius: 0.5rem; padding: 2rem; transition: var(--transition-smooth);">
      <h2 style="font-size: 1.5rem; margin-bottom: 0.5rem;">
        <a href="{{ post.url | relative_url }}" style="color: var(--color-primary);">{{ post.title }}</a>
      </h2>
      <p style="color: var(--color-text-muted); font-size: 0.85rem; margin-bottom: 1rem;">
        <i class="ph ph-calendar-blank"></i> {{ post.date | date: "%d/%m/%Y" }}
      </p>
      <p style="margin-bottom: 1.5rem;">
        {{ post.excerpt | strip_html | truncatewords: 30 }}
      </p>
      <a href="{{ post.url | relative_url }}" style="font-weight: 600; display: inline-flex; align-items: center; gap: 0.5rem;">
        Ler artigo completo <i class="ph ph-arrow-right"></i>
      </a>
    </article>
  {% endfor %}
</div>

<style>
.post-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px -5px rgba(29, 30, 90, 0.05);
    border-color: var(--color-primary-light);
}
</style>

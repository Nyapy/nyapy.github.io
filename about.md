---
layout: default
title: "About Jekyll"
permalink: /about/
---

# 📝 Jekyll 이란?

**Jekyll**은 Ruby 기반의 *정적 사이트 생성기(Static Site Generator)* 입니다.  
Markdown이나 HTML로 작성된 파일을 **Liquid 템플릿**을 통해  
정적 HTML로 변환해주는 역할을 합니다.

---

## ✨ 주요 특징

1. **Markdown 지원**
   - `.md` 파일로 글을 작성하면 자동으로 HTML로 변환됩니다.
   - 예: `# 제목` → `<h1>제목</h1>`

2. **Liquid 문법**
   - `{{ site.title }}` 같은 변수를 사용해서 동적으로 콘텐츠를 넣을 수 있습니다.
   - 반복문/조건문도 지원해요.

3. **정적 사이트**
   - 데이터베이스나 서버 로직이 필요 없습니다.
   - GitHub Pages에 그대로 올리면 자동으로 배포 가능!

---

## 🔧 예시 (Liquid 문법)

- 사이트 제목: **{{ site.title | default: "사이트 제목 없음" }}**
- 현재 시간: {{ site.time | date: "%Y-%m-%d %H:%M" }}

최근 글 3개:
{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

---

## 📂 Jekyll 프로젝트 기본 구조


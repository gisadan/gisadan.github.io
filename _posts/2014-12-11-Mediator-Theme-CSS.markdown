---
layout: post
title: ✚ Mediator CSS 수정하는 법
---

main.sass 를 텍스트 편집기로 불로온 후 기존에 있던 것을 지우고 아래와 같이 수정한다. 기존에 있던 것은 h1,h2가 구별이 안 됐고 또한, h3,h4,h5가 구별이 안되서 마크다운 문법을 쓰기에 불편했다.
다음과 같이 수정한다면 원래대로 마크다운 문법을 쓸 수 있을 것이다.


~~~
.post-content
    width: 100%
    font-family: Menlo
    color: #333
    h1, h2, h3
      font-family: Verdana
    h3
      letter-spacing: -0.02em
      font-weight: 700
      font-style: Verdana
      font-size: 1.5em
      line-height: 1.43
      margin: 0
      font-family: Verdana
      margin-bottom: 4px
    h4
      letter-spacing: -0.02em
      font-weight: 700
      font-style: Verdana
      font-size: 1.25em
      line-height: 1.3
      margin: 0
      font-family: Verdana
      margin-bottom: 4px
    h5
      letter-spacing: -0.02em
      font-weight: 700
      font-style: Verdana
      font-size: 1em
      line-height: 1.2
      margin: 0
      font-family: Verdana
      margin-bottom: 4px
    h1
      letter-spacing: -0.02em
      font-weight: 700
      font-style: Verdana
      font-size: 2.25em
      line-height: 1.5
      margin: 0
      font-family: $font-sans
      margin-bottom: 4px

    h2
      letter-spacing: -0.02em
      font-weight: 700
      font-style: Verdana
      font-size: 1.75em
      line-height: 1.4
      padding-top: 31px
      margin-bottom: 4px
    p
      font-weight: 400
      font-style: Menlo
      font-size: 17px
      line-height: 1.5
      margin: 0
      padding-bottom: 30px
      color: #333
      -webkit-hyphens: auto
      -moz-hyphens: auto
      hyphens: auto
~~~

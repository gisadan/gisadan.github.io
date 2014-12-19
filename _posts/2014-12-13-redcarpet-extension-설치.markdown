---  
layout: post  
title: ✚ 마크다운 문법 중 코드블럭, 취소선 등이 되지 않을 때  
---  

코드 관련 글을 포스팅하다가 갑자기 push에서 오류가 나기 시작했다. 왜 이런 오류가 발생했을까?에 대해 계속해서 고민해본 결과 마크다운으로 작성한 내용중에 코드가 들어가면 그것을 인식하여 오류가 나는 것이었다. 이런 오류를 막기 위해 마크다운 문법중에는 "fenced code block"이라는 아주 좋은 기능이 있다. 보통은 ` ``` ` 혹은 `~~~`로 작동하는데 도통 무엇이 문제인지 아무리 저 문법을 사용해도 되지가 않았다. 이를 해결하기 위해 여러 차례 redcarpet을 재설치하려고 시간을 썼지만, 제대로 설치되지 않았다는 메일만 받기 일쑤였다. 열심히 구글링을 하면서 여러 방법을 시도했지만 번번히 실패했고, 우연히 누가 config.yml파일의 내용을 올려둔 것을 보고 내것과 다르다는 것을 발견했다. 그래서 그것을 그대로 적용했더니 성공적으로 작동했다.  

하는 방법은 다음과 같다.▼   
1. config.yml 파일을 텍스트 편집기로 연다.  
2. 맨위에 Build settings가 있을 가능성이 크다.  
3. 그리고 아래 보면 markdown: redcarpet 이라고 되어 있을텐데 나는 그 밑에 부터 없었다.  
4. 그래서 아래 보이는 것처럼 redcarpet: extensions를 추가했다.  
5. 그러니 보이기 시작했다.  

~~~
# Build settings
markdown: redcarpet
redcarpet:
    extensions: ["no_intra_emphasis", "fenced_code_blocks", "autolink", "strikethrough", "superscript", "with_toc_data", "tables"]

highlighter: pygments

permalink: pretty
~~~
{:.language-ruby}

---
2014-12-19 추가

* kramdown
~~~
# Build settings
markdown: kramdown
kramdown:
    input: GFM
kramdown:
  auto_ids:      true
  footnote_nr:   1
  entity_output: as_char
  toc_levels:    1..6
  smart_quotes:  lsquo,rsquo,ldquo,rdquo
  use_coderay:   true

  coderay:
    coderay_wrap:              div
    coderay_line_numbers:      nil
    coderay_line_number_start: 1
    coderay_tab_width:         4
    coderay_bold_every:        10
    coderay_css:               style


highlighter: pygments
permalink: /:title/
~~~
{:.language-ruby}

* redcarpet
~~~
# Build settings
markdown: redcarpet
highlighter: pygments
permalink: /:title/

redcarpet:
    extensions: 
      - no_intra_emphasis
      - fenced_code_blocks
      - tables
      - strikethrough
      - superscript
      - autolink
      - hard_wrap
      - footnotes
~~~
{:.language-ruby}

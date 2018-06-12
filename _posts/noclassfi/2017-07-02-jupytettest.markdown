---
layout: "jupyter"
title: "jupytettest"
date: "2017-07-02 13:22"
categories:
---
<div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#45348;&#51060;&#48260;-&#44160;&#49353;&#50612;">&#45348;&#51060;&#48260; &#44160;&#49353;&#50612;<a class="anchor-link" href="#&#45348;&#51060;&#48260;-&#44160;&#49353;&#50612;">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>
<span class="kn">from</span> <span class="nn">bs4</span> <span class="k">import</span> <span class="n">BeautifulSoup</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">html</span><span class="o">=</span><span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;http://naver.com&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">text</span>
<span class="n">soup</span><span class="o">=</span><span class="n">BeautifulSoup</span><span class="p">(</span><span class="n">html</span><span class="p">,</span><span class="s1">&#39;html.parser&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tag_list</span><span class="o">=</span><span class="n">soup</span><span class="o">.</span><span class="n">select</span><span class="p">(</span><span class="s1">&#39;.PM_CL_realtimeKeyword_rolling .ah_item .ah_k&#39;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tag_list</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt output_prompt">Out[6]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>[&lt;span class=&#34;ah_k&#34;&gt;곽정은&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;강경화&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;캐릭터 커뮤니티&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;인천여아살인사건&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;노회찬&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;장미인애&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;런닝맨&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;윤손하&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;서세원&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;워너원&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;나혜미&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;지아이제인&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;안경환 아들&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;영화&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;내딸의남자들&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;베트남&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;수요미식회 스테이크&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;연애 플레이 리스트&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;ebs중학&lt;/span&gt;,
 &lt;span class=&#34;ah_k&#34;&gt;셜록홈즈 그림자게임&lt;/span&gt;]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">idx</span><span class="p">,</span> <span class="n">tag</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">tag_list</span><span class="p">,</span><span class="mi">1</span><span class="p">):</span> <span class="c1">#시작을 1로 한다.</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">idx</span><span class="p">,</span><span class="n">tag</span><span class="o">.</span><span class="n">text</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt"></div>
<div class="output_subarea output_stream output_stdout output_text">
<pre>1 곽정은
2 강경화
3 캐릭터 커뮤니티
4 인천여아살인사건
5 노회찬
6 장미인애
7 런닝맨
8 윤손하
9 서세원
10 워너원
11 나혜미
12 지아이제인
13 안경환 아들
14 영화
15 내딸의남자들
16 베트남
17 수요미식회 스테이크
18 연애 플레이 리스트
19 ebs중학
20 셜록홈즈 그림자게임
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#45348;&#51060;&#48260;-&#48660;&#47196;&#44536;-&#44160;&#49353;">&#45348;&#51060;&#48260; &#48660;&#47196;&#44536; &#44160;&#49353;<a class="anchor-link" href="#&#45348;&#51060;&#48260;-&#48660;&#47196;&#44536;-&#44160;&#49353;">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#url=&quot;https://search.naver.com/search.naver?where=post&amp;sm=tab_pge&amp;query=askdjango&amp;st=sim&amp;date_option=0&amp;date_from=&amp;date_to=&amp;dup_remove=1&amp;post_blogurl=&amp;post_blogurl_without=&amp;srchby=all&amp;nso=&amp;ie=utf8&amp;start=1&quot;</span>
<span class="kn">from</span> <span class="nn">collections</span> <span class="k">import</span> <span class="n">OrderedDict</span> <span class="c1"># 순서가 있는 사전</span>
<span class="kn">from</span> <span class="nn">itertools</span> <span class="k">import</span> <span class="n">count</span> <span class="c1"># 무한히 카운트하는 것</span>


<span class="k">def</span> <span class="nf">naver_blog_search</span><span class="p">(</span><span class="n">q</span><span class="p">,</span><span class="n">max_page</span><span class="o">=</span><span class="kc">None</span><span class="p">):</span>
    <span class="c1">#url=&quot;https://search.naver.com/search.naver?where=post&amp;query=askdjango&amp;start=1&quot;</span>
    <span class="n">url</span><span class="o">=</span><span class="s2">&quot;https://search.naver.com/search.naver&quot;</span>

    <span class="n">post_dict</span><span class="o">=</span><span class="n">OrderedDict</span><span class="p">()</span>

    <span class="k">for</span> <span class="n">page</span> <span class="ow">in</span> <span class="n">count</span><span class="p">(</span><span class="mi">1</span><span class="p">):</span> <span class="c1">#1페이지 부터 시작</span>
        <span class="n">params</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;where&quot;</span><span class="p">:</span><span class="s2">&quot;post&quot;</span><span class="p">,</span>
        <span class="s2">&quot;query&quot;</span><span class="p">:</span><span class="s2">&quot;askdjango&quot;</span><span class="p">,</span>
        <span class="s2">&quot;start&quot;</span><span class="p">:(</span><span class="n">page</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span><span class="o">*</span><span class="mi">10</span><span class="o">+</span><span class="mi">1</span><span class="p">,</span>
        <span class="p">}</span>
        <span class="n">html</span><span class="o">=</span><span class="n">requests</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="n">url</span><span class="p">,</span><span class="n">params</span><span class="o">=</span><span class="n">params</span><span class="p">)</span><span class="o">.</span><span class="n">text</span>
        <span class="n">soup</span><span class="o">=</span><span class="n">BeautifulSoup</span><span class="p">(</span><span class="n">html</span><span class="p">,</span><span class="s1">&#39;html.parser&#39;</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">tag</span> <span class="ow">in</span> <span class="n">soup</span><span class="o">.</span><span class="n">select</span><span class="p">(</span><span class="s1">&#39;.sh_blog_title&#39;</span><span class="p">):</span>
            <span class="k">if</span> <span class="n">tag</span><span class="p">[</span><span class="s1">&#39;href&#39;</span><span class="p">]</span> <span class="ow">in</span> <span class="n">post_dict</span><span class="p">:</span>
                <span class="k">return</span> <span class="n">post_dict</span>

            <span class="n">post_dict</span><span class="p">[</span><span class="n">tag</span><span class="p">[</span><span class="s1">&#39;href&#39;</span><span class="p">]]</span><span class="o">=</span><span class="n">tag</span><span class="o">.</span><span class="n">text</span>

        <span class="k">if</span> <span class="n">max_page</span> <span class="ow">and</span> <span class="p">(</span><span class="n">page</span> <span class="o">&gt;=</span> <span class="n">max_page</span><span class="p">):</span>
            <span class="k">break</span>

        <span class="k">return</span> <span class="n">post_dict</span>


</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">naver_blog_search</span><span class="p">(</span><span class="s1">&#39;AskDjango&#39;</span><span class="p">,</span><span class="mi">3</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area"><div class="prompt output_prompt">Out[18]:</div>


<div class="output_text output_subarea output_execute_result">
<pre>OrderedDict([(&#39;http://myjorney.tistory.com/26&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리 18) 파이썬 클래스...&#39;),
             (&#39;http://myjorney.tistory.com/2&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리)2.파이썬의 기본...&#39;),
             (&#39;http://myjorney.tistory.com/4&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리3)python 파이썬 들여쓰기...&#39;),
             (&#39;http://myjorney.tistory.com/23&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리 17) 파이썬 file...&#39;),
             (&#39;http://myjorney.tistory.com/1&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리1_파이썬의 코드 실행방법...&#39;),
             (&#39;http://myjorney.tistory.com/21&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리 16) 파이썬 인코딩...&#39;),
             (&#39;http://the7mincheol.blog.me/220947602901&#39;,
              &#39;2017.03 멜론 노래 검색기 (출처: askdjango)&#39;),
             (&#39;http://myjorney.tistory.com/15&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리 12) 파이썬 빌트인함수...&#39;),
             (&#39;http://the7mincheol.blog.me/220940162131&#39;,
              &#39;2017.02 네이버 맞춤법 검사기 (출처: askdjango)&#39;),
             (&#39;http://myjorney.tistory.com/28&#39;,
              &#39;Askdjango) 파이썬 기본문법 정리 19) 파이썬 호출...&#39;)])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span>
</pre></div>

</div>
</div>
</div>

</div>
    </div>
  </div>

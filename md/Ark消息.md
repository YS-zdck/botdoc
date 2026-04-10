 <div class="theme-default-content content__default"><h1 id="ark-消息"><a href="#ark-消息" class="header-anchor">#</a> ARK 消息</h1> <div class="custom-block tip"><p class="custom-block-title">说明</p> <p>主动消息 ARK：默认开放可用。
被动消息 ARK：达到准入条件的开发者，向平台运营申请后获得权限。</p></div> <table><thead><tr><th></th> <th><strong>单聊</strong></th> <th><strong>群聊</strong></th> <th><strong>文字子频道</strong></th> <th><strong>频道私信</strong></th></tr></thead> <tbody><tr><td>机器人接收</td> <td>-</td> <td>-</td> <td>-</td> <td>-</td></tr> <tr><td>机器人发送</td> <td>支持</td> <td>支持</td> <td>支持</td> <td>支持</td></tr></tbody></table> <h2 id="发送方式"><a href="#发送方式" class="header-anchor">#</a> 发送方式</h2> <p>选择合适的 ARK 模版发送，模版的有预设变量，变量类型可以是 字符串、数组、URL等。</p> <div class="language- line-numbers-mode"><pre class="language-text codecopy-enabled"><code>// 模版CASE，其中#META_LIST#类型为数组、#META_URL#类型为 URL 其他为文本
{
  "app": "com.tencent.miniapp",
  "view": "detail",
  "ver": "0.0.0.1",
  "desc": "#DESC#",
  "prompt": "[QQ小程序]#PROMPT#",
  "meta": {
    "detail": {
      "title": "#TITLE#",
      "desc": "#META_DESC#",
      "url": "#META_URL#",
      "list": "#META_LIST#"
    }
  }
}

// 发送CASE
{
  "ark": {
    "template_id": 23,
    "kv": [
      {
        "key": "#DESC#",
        "value": "机器人订阅消息"
      },
      {
        "key": "#PROMPT#",
        "value": "XX机器人"
      },
      {
        "key": "#TITLE#",
        "value": "XX机器人消息"
      },
      {
        "key": "#META_URL#",
        "value": "http://domain.com/"
      },
      {
        "key": "#META_LIST#",
        "obj": [
          {
            "obj_kv": [
              {
                "key": "name",
                "value": "aaa"
              },
              {
                "key": "age",
                "value": "3"
              }
            ]
          },
          {
            "obj_kv": [
              {
                "key": "name",
                "value": "bbb"
              },
              {
                "key": "age",
                "value": "4"
              }
            ]
          }
        ]
      }
    ]
  }
}
</code><i class="code-copy" title="Copy to clipboard"><svg style="color:#aaa;font-size:14px" t="1572422231464" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3201" width="14" height="14"><path d="M866.461538 39.384615H354.461538c-43.323077 0-78.769231 35.446154-78.76923 78.769231v39.384616h472.615384c43.323077 0 78.769231 35.446154 78.769231 78.76923v551.384616h39.384615c43.323077 0 78.769231-35.446154 78.769231-78.769231V118.153846c0-43.323077-35.446154-78.769231-78.769231-78.769231z m-118.153846 275.692308c0-43.323077-35.446154-78.769231-78.76923-78.769231H157.538462c-43.323077 0-78.769231 35.446154-78.769231 78.769231v590.769231c0 43.323077 35.446154 78.769231 78.769231 78.769231h512c43.323077 0 78.769231-35.446154 78.76923-78.769231V315.076923z m-354.461538 137.846154c0 11.815385-7.876923 19.692308-19.692308 19.692308h-157.538461c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h157.538461c11.815385 0 19.692308 7.876923 19.692308 19.692308v39.384615z m157.538461 315.076923c0 11.815385-7.876923 19.692308-19.692307 19.692308H216.615385c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h315.076923c11.815385 0 19.692308 7.876923 19.692307 19.692308v39.384615z m78.769231-157.538462c0 11.815385-7.876923 19.692308-19.692308 19.692308H216.615385c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h393.846153c11.815385 0 19.692308 7.876923 19.692308 19.692308v39.384615z" p-id="3202"></path></svg></i></pre> <div class="line-numbers-wrapper"><span class="line-number">1</span><br><span class="line-number">2</span><br><span class="line-number">3</span><br><span class="line-number">4</span><br><span class="line-number">5</span><br><span class="line-number">6</span><br><span class="line-number">7</span><br><span class="line-number">8</span><br><span class="line-number">9</span><br><span class="line-number">10</span><br><span class="line-number">11</span><br><span class="line-number">12</span><br><span class="line-number">13</span><br><span class="line-number">14</span><br><span class="line-number">15</span><br><span class="line-number">16</span><br><span class="line-number">17</span><br><span class="line-number">18</span><br><span class="line-number">19</span><br><span class="line-number">20</span><br><span class="line-number">21</span><br><span class="line-number">22</span><br><span class="line-number">23</span><br><span class="line-number">24</span><br><span class="line-number">25</span><br><span class="line-number">26</span><br><span class="line-number">27</span><br><span class="line-number">28</span><br><span class="line-number">29</span><br><span class="line-number">30</span><br><span class="line-number">31</span><br><span class="line-number">32</span><br><span class="line-number">33</span><br><span class="line-number">34</span><br><span class="line-number">35</span><br><span class="line-number">36</span><br><span class="line-number">37</span><br><span class="line-number">38</span><br><span class="line-number">39</span><br><span class="line-number">40</span><br><span class="line-number">41</span><br><span class="line-number">42</span><br><span class="line-number">43</span><br><span class="line-number">44</span><br><span class="line-number">45</span><br><span class="line-number">46</span><br><span class="line-number">47</span><br><span class="line-number">48</span><br><span class="line-number">49</span><br><span class="line-number">50</span><br><span class="line-number">51</span><br><span class="line-number">52</span><br><span class="line-number">53</span><br><span class="line-number">54</span><br><span class="line-number">55</span><br><span class="line-number">56</span><br><span class="line-number">57</span><br><span class="line-number">58</span><br><span class="line-number">59</span><br><span class="line-number">60</span><br><span class="line-number">61</span><br><span class="line-number">62</span><br><span class="line-number">63</span><br><span class="line-number">64</span><br><span class="line-number">65</span><br><span class="line-number">66</span><br><span class="line-number">67</span><br><span class="line-number">68</span><br><span class="line-number">69</span><br><span class="line-number">70</span><br></div></div><h2 id="数据结构与协议"><a href="#数据结构与协议" class="header-anchor">#</a> 数据结构与协议</h2> <p>消息发送接口 ark 字段值是一个 json object，具体字段如下：</p> <table><thead><tr><th><strong>属性</strong></th> <th><strong>类型</strong></th> <th><strong>必填</strong></th> <th><strong>说明</strong></th></tr></thead> <tbody><tr><td>template_id</td> <td>int</td> <td>是</td> <td>模版 id，管理端可获得或内邀申请获得 <br>以下默认可使用：<br><a href="/wiki/develop/api-v2/server-inter/message/type/template/template_23.html" class="">23 链接+文本列表模板|QQ机器人文档</a><br><a href="/wiki/develop/api-v2/server-inter/message/type/template/template_24.html" class="">24 文本+缩略图模板|QQ机器人文档</a><br><a href="/wiki/develop/api-v2/server-inter/message/type/template/template_37.html" class="">37 大图模板|QQ机器人文档</a></td></tr> <tr><td>kv</td> <td>array</td> <td>是</td> <td>{key: xxx, value: xxx}，模版内变量与填充值的kv映射</td></tr></tbody></table> <p>特别：当预设变量是数组时，kv数组元素的结构调整为：</p> <div class="language-json line-numbers-mode"><pre class="language-json codecopy-enabled"><code><span class="token comment">// 举个例子</span>
<span class="token punctuation">{</span>
    <span class="token string">"key: xxx"</span><span class="token punctuation">,</span> 
    <span class="token property">"obj"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span><span class="token property">"obj_kv"</span><span class="token operator">:</span><span class="token punctuation">[</span><span class="token punctuation">{</span><span class="token property">"key"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">,</span> <span class="token property">"value"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span><span class="token property">"key"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">,</span> <span class="token property">"value"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token comment">//一个 obj_kv 可以多个数组元素</span>
        <span class="token punctuation">{</span><span class="token property">"obj_kv"</span><span class="token operator">:</span><span class="token punctuation">[</span><span class="token punctuation">{</span><span class="token property">"key"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">,</span> <span class="token property">"value"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">}</span><span class="token punctuation">,</span> <span class="token punctuation">{</span><span class="token property">"key"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">,</span> <span class="token property">"value"</span><span class="token operator">:</span> <span class="token string">"xxx"</span><span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span>
        <span class="token comment">// 可以多个 obj_kv</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>

</code><i class="code-copy" title="Copy to clipboard"><svg style="color:#aaa;font-size:14px" t="1572422231464" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3201" width="14" height="14"><path d="M866.461538 39.384615H354.461538c-43.323077 0-78.769231 35.446154-78.76923 78.769231v39.384616h472.615384c43.323077 0 78.769231 35.446154 78.769231 78.76923v551.384616h39.384615c43.323077 0 78.769231-35.446154 78.769231-78.769231V118.153846c0-43.323077-35.446154-78.769231-78.769231-78.769231z m-118.153846 275.692308c0-43.323077-35.446154-78.769231-78.76923-78.769231H157.538462c-43.323077 0-78.769231 35.446154-78.769231 78.769231v590.769231c0 43.323077 35.446154 78.769231 78.769231 78.769231h512c43.323077 0 78.769231-35.446154 78.76923-78.769231V315.076923z m-354.461538 137.846154c0 11.815385-7.876923 19.692308-19.692308 19.692308h-157.538461c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h157.538461c11.815385 0 19.692308 7.876923 19.692308 19.692308v39.384615z m157.538461 315.076923c0 11.815385-7.876923 19.692308-19.692307 19.692308H216.615385c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h315.076923c11.815385 0 19.692308 7.876923 19.692307 19.692308v39.384615z m78.769231-157.538462c0 11.815385-7.876923 19.692308-19.692308 19.692308H216.615385c-11.815385 0-19.692308-7.876923-19.692308-19.692308v-39.384615c0-11.815385 7.876923-19.692308 19.692308-19.692308h393.846153c11.815385 0 19.692308 7.876923 19.692308 19.692308v39.384615z" p-id="3202"></path></svg></i></pre> <div class="line-numbers-wrapper"><span class="line-number">1</span><br><span class="line-number">2</span><br><span class="line-number">3</span><br><span class="line-number">4</span><br><span class="line-number">5</span><br><span class="line-number">6</span><br><span class="line-number">7</span><br><span class="line-number">8</span><br><span class="line-number">9</span><br><span class="line-number">10</span><br></div></div></div> <footer class="page-edit"><!----> <div class="last-updated"><span class="prefix">上次更新:</span> <span class="time">5/21/2025, 5:23:04 PM</span></div></footer> <div class="page-nav"><p class="inner"><span class="prev">
      ←
      <a href="/wiki/develop/api-v2/server-inter/message/type/sticker.html" class="prev">
        表情消息
      </a></span> <span class="next"><a href="/wiki/develop/api-v2/server-inter/message/type/embed.html" class="">
        Embed 消息
      </a>
      →
    </span></p></div> 
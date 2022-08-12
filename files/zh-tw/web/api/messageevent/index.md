---
title: MessageEvent
slug: Web/API/MessageEvent
tags:
  - WebSockets
translation_of: Web/API/MessageEvent
original_slug: WebSockets/WebSockets_reference/MessageEvent
---
<p>當伺服器傳來資料時，客戶端會收到一個 <code>MessageEvent</code>，由 <code>WebSocket</code> 物件 <code>onmessage</code> 表示的監聽器接收。</p>

<h2 id="Attributes">屬性</h2>

<table>
 <tbody>
  <tr>
   <td class="header">屬性</td>
   <td class="header">形態</td>
   <td class="header">描述</td>
  </tr>
  <tr>
   <td><code>data</code></td>
   <td>{{ domxref("DOMString") }} | {{ domxref("Blob") }} | <a href="/zh_tw/JavaScript_typed_arrays/ArrayBuffer"><code>ArrayBuffer</code></a></td>
   <td>伺服器傳來的資料。</td>
  </tr>
 </tbody>
</table>

<h2 id="規範">規範</h2>

{{Specifications}}

<h2 id="瀏覽器兼容">瀏覽器兼容</h2>

{{Compat("api.MessageEvent")}}

<h2 id="參見">參見</h2>

<ul>
 <li><a href="/zh_tw/WebSockets/WebSockets_reference/WebSocket"><code>WebSocket</code></a></li>
</ul>
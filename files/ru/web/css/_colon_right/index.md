---
title: ':right'
slug: 'Web/CSS/:right'
translation_of: 'Web/CSS/:right'
---
<div>{{ CSSRef() }}</div>

<p>The <strong><code>:right</code></strong> CSS <a href="/en/CSS/@page" title="@page">page</a> <a href="/en/CSS/Pseudo-classes" title="Pseudo-classes">pseudo-class</a> matches any right page when printing a page. It allows you to describe the styling of right-side pages.</p>

<pre class="brush: css no-line-numbers">/* Selects the content on the right-hand pages while printing */
@page :right {
  margin: 2in 3in;
}</pre>

<p>Whether the page is left or right is decided by the major writing direction of the document. For example, if the first page has a major writing direction of left-to-right then it will be a <code>:right</code> page and if it has a major writing direction of right-to-left then it will be a <code>{{ Cssxref(":left") }}</code> page.</p>

<div class="note"><strong>Note:</strong> Вы можете не менять все CSS-свойства, а поменять только margin, padding, border, и background для страницы. Все остальные CSS-свойства будут проигнорированы и изменения будут применены только для страницы, но не для её содержимого.</div>

<h2 id="Синтаксис">Синтаксис</h2>

{{csssyntax}}

<h2 id="Примеры">Примеры</h2>

<pre class="brush: css">@page :right {
  margin: 2in 3in;
}
</pre>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость_с_браузерами">Совместимость с браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li>{{ Cssxref("@page") }}, {{ Cssxref(":first") }}, {{ Cssxref(":left") }}</li>
</ul>
---
title: top
slug: Web/CSS/top
tags:
  - CSS
  - CSS Позиционирование
  - CSS-свойство
  - Справка
translation_of: Web/CSS/top
---
<div>{{CSSRef}}</div>

<p><a href="/ru/docs/Web/CSS" title="CSS">CSS</a> свойство <strong><code>top</code></strong> частично определяет вертикальную позицию позиционируемого элемента. Оно не влияет на непозиционируемые элементы (т.е. <strong><code>top</code></strong> не применится, если задано <code>position: static</code>).</p>

<div>{{EmbedInteractiveExample("pages/css/top.html")}}</div>

<p>Эффект свойства <code>top</code> зависит от того, как позиционируется элемент (то есть от значения свойства {{cssxref("position")}}):</p>

<ul>
 <li>Когда задано <code>position: absolute</code> или <code>fixed</code> — значение свойства <code>top</code> устанавливается как расстояние между верхней гранью элемента и верхней гранью родительского контейнера.</li>
 <li>Когда задано <code>position: relative</code> — значение свойство <code>top</code> устанавливается как расстояние, на которое смещается верхний край элемента от нормальной позиции.</li>
 <li>Когда задано <code>position: sticky</code> — свойство <code>top</code> работает так, как при <code>position: relative</code> во время нахождения элемента внутри области просмотра, и как <code>position: fixed</code> вне области просмотра.</li>
 <li>Когда задано <code>position: static</code> — свойство <code>top</code> <em>не имеет никакого эффекта</em>.</li>
</ul>

<p>Когда заданы оба свойства <code>top</code> и {{cssxref("bottom")}}, а свойство {{cssxref("position")}} установлено как <code>absolute</code> или <code>fixed</code>, то оба свойства <code>top</code> и {{cssxref("bottom")}} учитываются. Во всех остальных ситуациях, если {{cssxref("height")}} как-либо ограничена или <code>position</code> установлено как <code>relative</code>, то свойство <code>top</code> будет учтено, а {{cssxref("bottom")}} — проигнорировано.</p>

<h2 id="Синтаксис">Синтаксис</h2>

<pre class="brush:css no-line-numbers">/* Значения величин */
top: 3px;
top: 2.4em;

/* Процентные значения от высоты родительского блока */
top: 10%;

/* Ключевое слово */
top: auto;

/* Глобальные значения */
top: inherit;
top: initial;
top: unset;
</pre>

<h3 id="Значения">Значения</h3>

<dl>
 <dt>{{cssxref("&lt;length&gt;")}}</dt>
 <dd>Отрицательная, нулевая или положительная величина, которая представляет:
 <ul>
  <li>для <em>абсолютно позиционируемых элементов</em> &amp;mdash расстояние от верхнего края содержащего их блока;</li>
  <li>для <em>относительно позиционируемых элементов</em> &amp;mdash расстояние, на которое элемент смещается вниз, относительно своего положения в нормальном потоке.</li>
 </ul>
 </dd>
 <dt>{{cssxref("&lt;percentage&gt;")}}</dt>
 <dd>Процент от высоты родительского блока.</dd>
 <dt><code>auto</code></dt>
 <dd>Это ключевое слово, которое означает:
 <ul>
  <li>для <em>абсолютно спозиционированных элементов</em> — позиция элемента опирается на свойство {{cssxref("bottom")}}, пока <code>height: auto</code> обрабатывается как высота в зависимости от содержимого; если так же и <code>bottom: auto</code>, то элемент располагается так же, как при статическом позиционировании.</li>
  <li>для <em>относительно спозиционированных элементов</em> — расстояние элемента от его обычной позиции основано на свойстве {{cssxref ("bottom")}}; если значение <code>bottom</code> также <code>auto</code>, элемент вообще не перемещается по вертикали.</li>
 </ul>
 </dd>
 <dt><code>inherit</code></dt>
 <dd>Это ключевое слово указывает, что значение будет соответствовать вычисленному значению родительского блока (необязательно непосредственного родителя). Вычисляемое значение обрабатывается так же, как {{cssxref("&lt;length&gt;")}}, {{cssxref("&lt;percentage&gt;")}} или ключевое слово <code>auto</code>.</dd>
</dl>

<h3 id="Формальный_синтаксис">Формальный синтаксис</h3>

{{csssyntax}}

<h2 id="Пример">Пример</h2>

<pre class="brush: css">/* Для body могут быть использованы единицы px, также и для div */
body{
  width: 100%;
  height: 100%;
}

/* div теперь может использовать значения в процентах (body ширина и высота установлены) */
div {
  position: absolute;
  left: 15%;
  top: 30%;
  bottom: 30%;
  width: 70%;
  height: 40%;
  text-align: left;
  border: 3px rgb(0,0,0) solid;
}</pre>

<pre class="brush: html"> &lt;?xml version="1.0" encoding="utf-8"?&gt;
 &lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
           "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
 &lt;html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"&gt;
   &lt;head&gt;
     &lt;meta http-equiv="Content-Type" content="application/xhtml+xml" /&gt;
     &lt;title&gt;Mozilla.org height top left width percentage CSS&lt;/title&gt;
     &lt;style type="text/css"&gt;
       /* Для body могут быть использованы единицы px, также и для div */
       body {
         width: 100%;
         height: 100%;
       }
       /* div теперь может использовать значения в процентах (body ширина и высота установлены) */
       div {
         position: absolute;
         left: 15%;
         top: 30%;
         bottom: 30%;
         width: 70%;
         height: 40%;
         text-align: left;
         border: 3px rgb(0,0,0) solid;
       }
     &lt;/style&gt;
   &lt;/head&gt;
   &lt;body&gt;
      &lt;center&gt;
        &lt;div&gt;
             ...Some content...
        &lt;/div&gt;
      &lt;/center&gt;

   &lt;/body&gt;
 &lt;/html&gt;</pre>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость_с_браузерами">Совместимость с браузерами</h2>

<p>{{Compat}}</p>
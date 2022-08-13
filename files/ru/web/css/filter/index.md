---
title: filter
slug: Web/CSS/filter
tags:
  - CSS
  - SVG
  - SVG фильтр
  - filter
  - Свойство CSS
  - Ссылка
translation_of: Web/CSS/filter
---
<div>{{CSSRef}}{{SeeCompatTable}}</div>

<h2 id="Описание">Описание</h2>

<p><a href="https://developer.mozilla.org/en-US/docs/Web/CSS">CSS</a> свойство <strong><code>filter</code></strong>  позволяет вам применять к элементу такие графические эффекты, как размытие и смещение цвета. Фильтры обычно используются для регулировки рендеринга изображений, фонов и рамок.</p>

<p>В стандарт CSS включены несколько функций, которые обеспечивают предопределённые эффекты. Вы также можете ссылаться на SVG фильтр с URL-адресом на <a href="/en-US/docs/Web/SVG/Element/filter">элемент фильтра SVG</a>.</p>

<div class="note"><strong>Предупреждение:</strong> Старые версии (с 4.0 до 9.0) браузера Windows Internet Explorer поддерживают нестандартный <a class="external" href="http://msdn.microsoft.com/en-us/library/ms532853(v=vs.85).aspx">"filter"</a>, который с тех пор устарел.</div>

<p>{{cssinfo}}</p>

<h2 id="Синтаксис">Синтаксис</h2>

<pre class="brush:css">filter: url(resources.svg);
filter: blur(5px);
filter: brightness(0.4);
filter: contrast(200%);
filter: drop-shadow(16px 16px 20px blue);
filter: grayscale(50%);
filter: hue-rotate(90deg);
filter: invert(75%);
filter: opacity(25%);
filter: saturate(30%);
filter: sepia(60%);

/* Применение нескольких фильтров */
filter: contrast(175%) brightness(3%);

/* Глобальные значения */
filter: inherit;
filter: initial;
filter: unset;
</pre>

<p>С помощью функции, используйте:</p>

<pre class="syntaxbox">filter: &lt;filter-function&gt; [&lt;filter-function&gt;]* | none
</pre>

<p>Для ссылки на SVG {{SVGElement("filter")}} элемент, используйте:</p>

<pre class="syntaxbox">filter: url(svg-url#element-id)
</pre>

<h3 id="Формальный_синтаксис">Формальный синтаксис</h3>

{{csssyntax}}

<h2 id="Примеры">Примеры</h2>

<p>Примеры использования предопределённых функций показаны ниже. См. каждую функцию для конкретного примера.</p>

<pre class="brush: css">.mydiv { filter: grayscale(50%) }

/* сделать все изображения серыми на 50% и размыть на 10px */
img {
  filter: grayscale(0.5) blur(10px);
}</pre>

<p>Примеры использования функции URL с SVG ресурсом показаны ниже.</p>

<pre class="brush: css">.target { filter: url(#c1); }

.mydiv { filter: url(commonfilters.xml#large-blur) }
</pre>

<h2 id="Функции">Функции</h2>

<p>Для использования CSS-свойства <code>filter</code>, вы указываете значение для одной из выбранных функций. Если это значение недействительно, функция возвращает "none." За исключением тех случаев, когда функции, которые принимают значение, выраженное в процентах (34%), также принимают значение, выраженное как десятичная дробь (0.34).</p>

<h3 id="url"><code>url()</code></h3>

<p>The url() function takes the location of an XML file that specifies an SVG filter, and may include an anchor to a specific filter element.</p>

<pre class="brush: css">filter: url(resources.svg#c1)
</pre>

<h3 id="blur_размытие"><code>blur() [размытие]</code></h3>

<p>Applies a Gaussian blur to the input image. The value of ‘radius’ defines the value of the standard deviation to the Gaussian function, or how many pixels on the screen blend into each other, so a larger value will create more blur. If no parameter is provided, then a value <code>0</code> is used. The parameter is specified as a CSS length, but does not accept percentage values.</p>

<pre class="brush: css">filter: blur(5px)
</pre>

<div id="blur_example" class="hidden">
<pre class="brush: html">  &lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form.jpg" id="img1" class="internal default" src="/files/3710/Test_Form_2.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form.jpg" id="img2" class="internal default" src="/files/3710/Test_Form_2.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg id="img3" viewbox="0 0 233 176"&gt;
  &lt;filter id="svgBlur" x="-5%" y="-5%" width="110%" height="110%" &gt;
    &lt;feGaussianBlur in="SourceGraphic" stdDeviation="5" /&gt;
  &lt;/filter&gt;
  &lt;image xlink:href="/files/3710/Test_Form_2.jpeg" filter="url(#svgBlur)" x="5%" y="5%" width="212px" height="161px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_s.jpg" id="img4" class="internal default" src="/files/3711/Test_Form_2_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter:blur(5px);
  -webkit-filter:blur(5px);
  -o-filter:blur(5px);
  -ms-filter:blur(5px);
  filter:blur(5px); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  height: 100%;
  width: 85%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<pre class="brush: html">&lt;svg style="position: absolute; top: -99999px" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;filter id="svgBlur" x="-5%" y="-5%" width="110%" height="110%"&gt;
    &lt;feGaussianBlur in="SourceGraphic" stdDeviation="5"/&gt;
  &lt;/filter&gt;
&lt;/svg&gt;</pre>

<p>{{EmbedLiveSample('blur_example','100%','236px','')}}</p>

<h3 id="brightness_яркость"><code>brightness() [яркость]</code></h3>

<p>Applies a linear multiplier to input image, making it appear more or less bright. A value of <code>0%</code> will create an image that is completely black. A value of <code>100%</code> leaves the input unchanged. Other values are linear multipliers on the effect. Values of an amount over <code>100%</code> are allowed, providing brighter results. If the ‘amount’ parameter is missing, a value of <code>1</code> is used.</p>

<pre class="brush: css">filter: brightness(0.5)</pre>

<pre class="brush: html">&lt;svg style="position: absolute; top: -99999px" xmlns="http://www.w3.org/2000/svg"&gt;
 &lt;filter id="brightness"&gt;
    &lt;feComponentTransfer&gt;
        &lt;feFuncR type="linear" slope="[amount]"/&gt;
        &lt;feFuncG type="linear" slope="[amount]"/&gt;
        &lt;feFuncB type="linear" slope="[amount]"/&gt;
    &lt;/feComponentTransfer&gt;
  &lt;/filter&gt;
&lt;/svg&gt;</pre>

<div id="brightness_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form.jpg" id="img1" class="internal default" src="/files/3708/Test_Form.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form.jpg" id="img2" class="internal default" src="/files/3708/Test_Form.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 286 217"&gt;
 &lt;filter id="brightness"&gt;
    &lt;feComponentTransfer&gt;
        &lt;feFuncR type="linear" slope="2"/&gt;
        &lt;feFuncG type="linear" slope="2"/&gt;
        &lt;feFuncB type="linear" slope="2"/&gt;
    &lt;/feComponentTransfer&gt;
  &lt;/filter&gt;
  &lt;image xlink:href="/files/3708/Test_Form.jpg" filter="url(#brightness)" width="286px" height="217px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_s.jpg" id="img4" class="internal default" src="/files/3709/Test_Form_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter:brightness(2);
  -webkit-filter:brightness(2);
  -o-filter:brightness(2);
  -ms-filter:brightness(2);
  filter:brightness(2); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  height:100%;
  width: 85%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('brightness_example','100%','231px','')}}</p>

<h3 id="contrast_контраст"><code>contrast() [контраст]</code></h3>

<p>Adjusts the contrast of the input. A value of <code>0%</code> will create an image that is completely black. A value of <code>100%</code> leaves the input unchanged. Values of amount over <code>100%</code> are allowed, providing results with less contrast. If the ‘amount’ parameter is missing, a value of <code>1</code> is used.</p>

<pre class="brush: css">filter: contrast(200%)
</pre>

<pre class="brush: html">&lt;svg style="position: absolute; top: -99999px" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;filter id="contrast"&gt;
    &lt;feComponentTransfer&gt;
      &lt;feFuncR type="linear" slope="[amount]" intercept="-(0.5 * [amount]) + 0.5"/&gt;
      &lt;feFuncG type="linear" slope="[amount]" intercept="-(0.5 * [amount]) + 0.5"/&gt;
      &lt;feFuncB type="linear" slope="[amount]" intercept="-(0.5 * [amount]) + 0.5"/&gt;
    &lt;/feComponentTransfer&gt;
  &lt;/filter&gt;
&lt;/svg&gt;
</pre>

<div id="contrast_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_3.jpeg" id="img1" class="internal default" src="/files/3712/Test_Form_3.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_3.jpg" id="img2" class="internal default" src="/files/3712/Test_Form_3.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 240 151"&gt;
 &lt;filter id="contrast"&gt;
    &lt;feComponentTransfer&gt;
      &lt;feFuncR type="linear" slope="2" intercept="-0.5"/&gt;
      &lt;feFuncG type="linear" slope="2" intercept="-0.5"/&gt;
      &lt;feFuncB type="linear" slope="2" intercept="-0.5"/&gt;
    &lt;/feComponentTransfer&gt;
  &lt;/filter&gt;
  &lt;image xlink:href="/files/3712/Test_Form_3.jpeg" filter="url(#contrast)" width="240px" height="151px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_s.jpg" id="img4" class="internal default" src="/files/3713/Test_Form_3_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter:contrast(200%);
  -webkit-filter:contrast(200%);
  -o-filter:contrast(200%);
  -ms-filter:contrast(200%);
  filter:contrast(200%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('contrast_example','100%','203px','')}}</p>

<h3 id="drop-shadow_тень"><code>drop-shadow() [тень]</code></h3>

<p>Applies a drop shadow effect to the input image. A drop shadow is effectively a blurred, offset version of the input image's alpha mask drawn in a particular color, composited below the image. The function accepts a parameter of type &lt;shadow&gt; (defined in CSS3 Backgrounds), with the exception that the ‘inset’ keyword is not allowed. This function is similar to the more established {{cssxref("box-shadow")}} property; the difference is that with filters, some browsers provide hardware acceleration for better performance. The parameters of the <code>&lt;shadow&gt;</code> parameter are as follows.</p>

<dl>
 <dt><code>&lt;offset-x&gt;</code> <code>&lt;offset-y&gt;</code> <small>(required)</small></dt>
 <dd>These are two {{cssxref("&lt;length&gt;")}} values to set the shadow offset. <code>&lt;offset-x&gt;</code> specifies the horizontal distance. Negative values place the shadow to the left of the element. <code>&lt;offset-y&gt;</code> specifies the vertical distance. Negative values place the shadow above the element. See {{cssxref("&lt;length&gt;")}} for possible units.<br>
 If both values are <code>0</code>, the shadow is placed behind the element (and may generate a blur effect if <code>&lt;blur-radius&gt;</code> and/or <code>&lt;spread-radius&gt;</code> is set).</dd>
 <dt><code>&lt;blur-radius&gt;</code> <small>(optional)</small></dt>
 <dd>This is a third {{cssxref("&lt;length&gt;")}} value. The larger this value, the bigger the blur, so the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it will be <code>0</code> (the shadow's edge is sharp).</dd>
 <dt><code>&lt;spread-radius&gt;</code> <small>(optional)</small></dt>
 <dd>This is a fourth {{cssxref("&lt;length&gt;")}} value. Positive values will cause the shadow to expand and grow bigger, and negative values will cause the shadow to shrink. If not specified, it will be <code>0</code> (the shadow will be the same size as the element). <br>
 Note: Webkit, and maybe other browsers, do not support this 4th length; it will not render if added.</dd>
 <dt><code>&lt;color&gt;</code> <small>(optional)</small></dt>
 <dd>See {{cssxref("&lt;color&gt;")}} values for possible keywords and notations. If not specified, the color depends on the browser. In Gecko (Firefox), Presto (Opera) and Trident (Internet Explorer), the value of the {{cssxref("color")}} property is used. On the other hand, WebKit's shadow is transparent and therefore useless if <code>&lt;color&gt;</code> is omitted.</dd>
</dl>

<pre class="brush: css">filter: drop-shadow(16px 16px 10px black)</pre>

<pre class="brush: html">&lt;svg style="position: absolute; top: -999999px" xmlns="http://www.w3.org/2000/svg"&gt;
 &lt;filter id="drop-shadow"&gt;
    &lt;feGaussianBlur in="SourceAlpha" stdDeviation="[radius]"/&gt;
    &lt;feOffset dx="[offset-x]" dy="[offset-y]" result="offsetblur"/&gt;
    &lt;feFlood flood-color="[color]"/&gt;
    &lt;feComposite in2="offsetblur" operator="in"/&gt;
    &lt;feMerge&gt;
      &lt;feMergeNode/&gt;
      &lt;feMergeNode in="SourceGraphic"/&gt;
    &lt;/feMerge&gt;
  &lt;/filter&gt;
&lt;/svg&gt;
</pre>

<div id="shadow_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4.jpeg" id="img1" class="internal default" src="/files/3714/Test_Form_4.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4.jpg" id="img2" class="internal default" src="/files/3714/Test_Form_4.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 239 187"&gt;
 &lt;filter id="drop-shadow"&gt;
    &lt;feGaussianBlur in="SourceAlpha" stdDeviation="5"/&gt;
    &lt;feOffset dx="16" dy="16"/&gt;
    &lt;feMerge&gt;
      &lt;feMergeNode/&gt;
      &lt;feMergeNode in="SourceGraphic"/&gt;
    &lt;/feMerge&gt;
 &lt;/filter&gt;
 &lt;image xlink:href="/files/3714/Test_Form_4.jpeg" filter="url(#drop-shadow)" width="213px" height="161px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4_s.jpg" id="img4" class="internal default" src="/files/3715/Test_Form_4_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4 distorded border - Original image" id="img11" class="internal default" src="/files/8467/Test_Form_4_irregular-shape_opacity-gradient.png" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4 distorded border - Live example" id="img12" class="internal default" src="/files/8467/Test_Form_4_irregular-shape_opacity-gradient.png" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;
        &lt;div class="svg-container"&gt;
          &lt;svg xmlns="http://www.w3.org/2000/svg" id="img13" viewbox="0 0 239 187"&gt;
            &lt;filter id="drop-shadow2"&gt;
              &lt;feGaussianBlur in="SourceAlpha" stdDeviation="4"/&gt;
              &lt;feOffset dx="8" dy="10"/&gt;
              &lt;feMerge&gt;
                &lt;feMergeNode/&gt;
                &lt;feMergeNode in="SourceGraphic"/&gt;
              &lt;/feMerge&gt;
            &lt;/filter&gt;
            &lt;image xlink:href="/files/8467/Test_Form_4_irregular-shape_opacity-gradient.png<span style="font-size: 1rem;">" filter="url(#drop-shadow2)" width="213px" height="161px" /&gt;</span>
          &lt;/svg&gt;
        &lt;div&gt;
      &lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_4 distorded border drop shadow - Static example" id="img14" class="internal default" src="/files/8469/Test_Form_4_irregular-shape_opacity-gradient_drop-shadow.png" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: drop-shadow(16px 16px 10px black);
  -webkit-filter: drop-shadow(16px 16px 10px black);
  -o-filter: drop-shadow(16px 16px 10px black);
  -ms-filter: drop-shadow(16px 16px 10px black);
  filter: drop-shadow(16px 16px 10px black);
}
#img12 {
  width:100%;
  height:auto;
  -moz-filter: drop-shadow(8px 9px 5px rgba(0,0,0,.8));
  -webkit-filter: drop-shadow(8px 9px 5px rgba(0,0,0,.8));
  -o-filter: drop-shadow(8px 9px 5px rgba(0,0,0,.8));
  -ms-filter: drop-shadow(8px 9px 5px rgba(0,0,0,.8));
  filter: drop-shadow(8px 9px 5px rgba(0,0,0,.8));
}
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
#irregular-shape {
  width: 64%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3, #img13 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('shadow_example','100%','300px','')}}</p>

<h3 id="grayscale_оттенки_серого"><code>grayscale() [оттенки серого]</code></h3>

<p>Converts the input image to grayscale. The value of ‘amount’ defines the proportion of the conversion. A value of <code>100%</code> is completely grayscale. A value of <code>0%</code> leaves the input unchanged. Values between <code>0%</code> and <code>100%</code> are linear multipliers on the effect. If the ‘amount’ parameter is missing, a value of <code>0</code> is used.</p>

<pre class="brush: css">filter: grayscale(100%)</pre>

<div id="grayscale_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_5.jpeg" id="img1" class="internal default" src="/files/3716/Test_Form_5.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_5.jpg" id="img2" class="internal default" src="/files/3716/Test_Form_5.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 276 184"&gt;
 &lt;filter id="grayscale"&gt;
    &lt;feColorMatrix type="matrix"
               values="0.2126 0.7152 0.0722 0 0
                       0.2126 0.7152 0.0722 0 0
                       0.2126 0.7152 0.0722 0 0
                       0 0 0 1 0"/&gt;
  &lt;/filter&gt;
  &lt;image xlink:href="/files/3716/Test_Form_5.jpeg" filter="url(#grayscale)" width="276px" height="184px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_5_s.jpg" id="img4" class="internal default" src="/files/3717/Test_Form_5_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter:grayscale(100%);
  -webkit-filter:grayscale(100%);
  -o-filter:grayscale(100%);
  -ms-filter:grayscale(100%);
  filter:grayscale(100%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('grayscale_example','100%','209px','')}}</p>

<h3 id="hue-rotate_изменение_оттенка"><code>hue-rotate() [изменение оттенка]</code></h3>

<p>Applies a hue rotation on the input image. The value of ‘<code>angle</code>’ defines the number of degrees around the color circle the input samples will be adjusted. A value of <code>0deg </code>leaves the input unchanged. If the ‘<code>angle</code>’ parameter is missing, a value of <code>0deg</code> is used. Though there is no maximum value, the effect of values above <code>360deg</code> wraps around.</p>

<pre class="brush: css">filter: hue-rotate(90deg)</pre>

<div id="huerotate_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_6.jpeg" id="img1" class="internal default" src="/files/3718/Test_Form_6.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_6.jpg" id="img2" class="internal default" src="/files/3718/Test_Form_6.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 266 190"&gt;
 &lt;filter id="hue-rotate"&gt;
    &lt;feColorMatrix type="hueRotate"
               values="90"/&gt;
  &lt;/filter&gt;
  &lt;image xlink:href="/files/3718/Test_Form_6.jpeg" filter="url(#hue-rotate)" width="266px" height="190px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_6_s.jpg" id="img4" class="internal default" src="/files/3719/Test_Form_6_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter:hue-rotate(90deg);
  -webkit-filter:hue-rotate(90deg);
  -o-filter:hue-rotate(90deg);
  -ms-filter:hue-rotate(90deg);
  filter:hue-rotate(90deg); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<pre class="brush: html">&lt;svg style="position: absolute; top: -999999px" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;filter id="svgHueRotate" &gt;
    &lt;feColorMatrix type="hueRotate" values="[angle]" /&gt;
  &lt;filter /&gt;
&lt;/svg&gt;</pre>

<p>{{EmbedLiveSample('huerotate_example','100%','221px','')}}</p>

<h3 id="invert_инвертирование"><code>invert() [инвертирование]</code></h3>

<p>Inverts the samples in the input image. The value of ‘<code>amount</code>’ defines the proportion of the conversion. A value of <code>100%</code> is completely inverted. A value of <code>0%</code> leaves the input unchanged. Values between <code>0%</code> and <code>100%</code> are linear multipliers on the effect. If the ‘<code>amount</code>’ parameter is missing, a value of <code>0</code> is used.</p>

<pre class="brush: css">filter: invert(100%)</pre>

<div id="invert_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_7.jpeg" id="img1" class="internal default" src="/files/3720/Test_Form_7.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_7.jpg" id="img2" class="internal default" src="/files/3720/Test_Form_7.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 183 276"&gt;
 &lt;filter id="invert"&gt;
    &lt;feComponentTransfer&gt;
        &lt;feFuncR type="table" tableValues="1 0"/&gt;
        &lt;feFuncG type="table" tableValues="1 0"/&gt;
        &lt;feFuncB type="table" tableValues="1 0"/&gt;
    &lt;/feComponentTransfer&gt;
 &lt;/filter&gt;
 &lt;image xlink:href="/files/3720/Test_Form_7.jpeg" filter="url(#invert)" width="183px" height="276px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_7_s.jpg" id="img4" class="internal default" src="/files/3721/Test_Form_7_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: invert(100%);
  -webkit-filter: invert(100%);
  -o-filter: invert(100%);
  -ms-filter: invert(100%);
  filter: invert(100%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('invert_example','100%','407px','')}}</p>

<h3 id="opacity_непрозрачность"><code>opacity() [непрозрачность]</code></h3>

<p>Applies transparency to the samples in the input image. The value of ‘<code>amount</code>’ defines the proportion of the conversion. A value of <code>0%</code> is completely transparent. A value of <code>100%</code> leaves the input unchanged. Values between <code>0%</code> and <code>100%</code> are linear multipliers on the effect. This is equivalent to multiplying the input image samples by amount. If the ‘<code>amount</code>’ parameter is missing, a value of <code>1</code> is used. This function is similar to the more established {{Cssxref("opacity")}} property; the difference is that with filters, some browsers provide hardware acceleration for better performance.</p>

<pre class="brush: css">filter: opacity(50%)</pre>

<div id="opacity_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_14.jpeg" id="img1" class="internal default" src="/files/3725/Test_Form_14.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_14.jpg" id="img2" class="internal default" src="/files/3725/Test_Form_14.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 276 183"&gt;
 &lt;filter id="opacity"&gt;
    &lt;feComponentTransfer&gt;
        &lt;feFuncA type="table" tableValues="0 0.5"&gt;
    &lt;/feComponentTransfer&gt;
 &lt;/filter&gt;
 &lt;image xlink:href="/files/3725/Test_Form_14.jpeg" filter="url(#opacity)" width="276px" height="183px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_14_s.jpg" id="img4" class="internal default" src="/files/3726/Test_Form_14_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: opacity(50%);
  -webkit-filter: opacity(50%);
  -o-filter: opacity(50%);
  -ms-filter: opacity(50%);
  filter: opacity(50%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('opacity_example','100%','210px','')}}</p>

<h3 id="saturate_насыщенность"><code>saturate() [насыщенность]</code></h3>

<p>Saturates the input image. The value of ‘<code>amount</code>’ defines the proportion of the conversion. A value of <code>0%</code> is completely un-saturated. A value of <code>100%</code> leaves the input unchanged. Other values are linear multipliers on the effect. Values of amount over <code>100%</code> are allowed, providing super-saturated results. If the ‘<code>amount</code>’ parameter is missing, a value of <code>1</code> is used.</p>

<pre class="brush: css">filter: saturate(200%)</pre>

<div id="saturate_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_9.jpeg" id="img1" class="internal default" src="/files/3722/Test_Form_9.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_9.jpg" id="img2" class="internal default" src="/files/3722/Test_Form_9.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 201 239"&gt;
 &lt;filter id="saturate"&gt;
    &lt;feColorMatrix type="saturate"
               values="2"/&gt;
 &lt;/filter&gt;
 &lt;image xlink:href="/files/3722/Test_Form_9.jpeg" filter="url(#saturate)" width="201px" height="239px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_9_s.jpg" id="img4" class="internal default" src="/files/3724/Test_Form_9_s.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: saturate(200%);
  -webkit-filter: saturate(200%);
  -o-filter: saturate(200%);
  -ms-filter: saturate(200%);
  filter: saturate(200%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('saturate_example','100%','332px','')}}</p>

<h3 id="sepia_сепия"><code>sepia() [сепия]</code></h3>

<p>Converts the input image to sepia. The value of ‘<code>amount</code>’ defines the proportion of the conversion. A value of 100% is completely sepia. A value of <code>0%</code> leaves the input unchanged. Values between <code>0%</code> and <code>100%</code> are linear multipliers on the effect. If the ‘<code>amount</code>’ parameter is missing, a value of <code>0</code> is used.</p>

<pre class="brush: css">filter: sepia(100%)</pre>

<div id="sepia_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;SVG Equivalent&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_12.jpeg" id="img1" class="internal default" src="/files/3727/Test_Form_12.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_12.jpg" id="img2" class="internal default" src="/files/3727/Test_Form_12.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;div class="svg-container"&gt;&lt;svg xmlns="http://www.w3.org/2000/svg" id="img3" viewbox="0 0 259 194"&gt;
 &lt;filter id="sepia"&gt;
    &lt;feColorMatrix type="matrix"
               values="0.393 0.769 0.189 0 0
                       0.349 0.686 0.168 0 0
                       0.272 0.534 0.131 0 0
                       0 0 0 1 0"/&gt;
 &lt;/filter&gt;
 &lt;image xlink:href="/files/3727/Test_Form_12.jpeg" filter="url(#sepia)" width="259px" height="194px" /&gt;
&lt;/svg&gt;&lt;div&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_12_s.jpg" id="img4" class="internal default" src="/files/3728/Test_Form_12_s.jpg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: sepia(100%);
  -webkit-filter: sepia(100%);
  -o-filter: sepia(100%);
  -ms-filter: sepia(100%);
  filter: sepia(100%); }
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('sepia_example','100%','229px','')}}</p>

<h2 id="Комбинирование_функций">Комбинирование функций</h2>

<p>You may combine any number of functions to manipulate the rendering. The following example enhances the contrast and brightness of the image.</p>

<pre class="brush: css">filter: contrast(175%) brightness(103%)</pre>

<div id="combination_example" class="hidden">
<pre class="brush: html">&lt;table class="standard-table"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th align="left" scope="col"&gt;Original image&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Live example&lt;/th&gt;
      &lt;th align="left" scope="col"&gt;Static example&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;&lt;img alt="Test_Form_8.jpeg" id="img1" class="internal default" src="/files/3729/Test_Form_8.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_8.jpg" id="img2" class="internal default" src="/files/3729/Test_Form_8.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
      &lt;td&gt;&lt;img alt="Test_Form_8_s.jpg" id="img4" class="internal default" src="/files/3730/Test_Form_8_s.jpeg" style="width: 100%;" /&gt;&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
</pre>

<pre class="brush: css">html {
  height:100%;
}
body {
  font: 14px/1.286 "Lucida Grande","Lucida Sans Unicode","DejaVu Sans",Lucida,Arial,Helvetica,sans-serif;
  color: rgb(51, 51, 51);
  height:100%;
  overflow:hidden;
}
#img2 {
  width:100%;
  height:auto;
  -moz-filter: contrast(175%) brightness(103%);
  -webkit-filter: contrast(175%) brightness(103%);
  -o-filter: contrast(175%) brightness(103%);
  -ms-filter: contrast(175%) brightness(103%);
  filter: contrast(175%) brightness(103%);
}
table.standard-table {
  border: 1px solid rgb(187, 187, 187);
  border-collapse: collapse;
  border-spacing: 0px;
  margin: 0px 0px 1.286em;
  width: 85%;
  height: 100%;
}
table.standard-table th {
  border: 1px solid rgb(187, 187, 187);
  padding: 0px 5px;
  background: none repeat scroll 0% 0% rgb(238, 238, 238);
  text-align: left;
  font-weight: bold;
}
table.standard-table td {
  padding: 5px;
  border: 1px solid rgb(204, 204, 204);
  text-align: left;
  vertical-align: top;
  width:25%;
  height:auto;
}
#img3 {
  height:100%;
}
</pre>
</div>

<p>{{EmbedLiveSample('combination_example','100%','209px','')}}</p>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость_с_браузерами">Совместимость с браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li><a class="internal" href="/en-US/docs/Applying_SVG_effects_to_HTML_content">Applying SVG effects to HTML content</a></li>
 <li>The {{Cssxref("mask")}} property</li>
 <li><a class="internal" href="/en-US/docs/Web/SVG">SVG</a></li>
 <li><a class="external" href="http://www.html5rocks.com/en/tutorials/filters/understanding-css/">Understanding CSS filters</a>, HTML5Rocks! article</li>
 <li><a class="external" href="http://techstream.org/Web-Design/CSS3-Image-Filters">CSS 3 filters</a> Tech Stream article</li>
 <li><a class="external" href="http://davidwalsh.name/css-filters">CSS filters</a> By David Walsh</li>
</ul>
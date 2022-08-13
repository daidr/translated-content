---
title: <color>
slug: Web/CSS/color_value
translation_of: Web/CSS/color_value
---
<div>{{CSSRef}}</div>

<p>Тип <strong><code>&lt;color&gt;</code></strong> <a href="/en-US/docs/Web/CSS">CSS</a> <a href="/en-US/docs/Web/CSS/CSS_Types">data type</a> предоставляет цвет в цветовом спектре <a class="external" href="https://en.wikipedia.org/wiki/SRGB">sRGB</a>. В  <code>&lt;color&gt;</code> может включать значения прозрачности Альфа-канала (<a class="external" href="https://en.wikipedia.org/wiki/Alpha_compositing">alpha-channel</a>), указывающие, как цвет <a href="https://www.w3.org/TR/2003/REC-SVG11-20030114/masking.html#SimpleAlphaBlending">сочетается</a> с его фоном.</p>

<p>В <code>&lt;color&gt;</code> может быть определена любым из следующих способов can.</p>

<ul>
 <li>Использование или подключённого свойства ведённого в параметр (например, <code>blue</code> или <code>transparent</code>)</li>
 <li>Использование <a href="https://en.wikipedia.org/wiki/RGB_color_model#Geometric_representation">кубической системы координат RGB</a> (via the #-hexadecimal or the <code>rgb()</code> and <code>rgba()</code> functional notations)<img alt="Цветовая модель представлена виде куба" src="https://en.wikipedia.org/wiki/RGB_color_model#/media/File:RGB_color_solid_cube.png" style="height: 200px; width: 200px;"></li>
 <li>Использование <a href="https://en.wikipedia.org/wiki/HSL_and_HSV">цилиндрической системы координат HSL</a> (через функциональные обозначения <code>hsl()</code> и <code>hsla()</code>) </li>
</ul>

<div class="note">
<p><strong>Примечание: </strong>В этой статье подробно описывается тип данных &lt;color&gt;. Дополнительные сведения об использовании цвета в HTML см. В разделе применение цвета к <a href="/en-US/docs/Web/HTML/Applying_color">элементам HTML с помощью CSS</a>.</p>
</div>

<h2 id="Синтаксис">Синтаксис </h2>

<p>Для типа данных задаётся <code>&lt;color&gt;</code>  с помощью одного из следующих параметров.</p>

<div class="note">
<p><strong>Примечание:</strong> значения <code>&lt;color&gt;</code> точно определены, их фактический внешний вид может отличаться (иногда значительно) от устройства к устройству. Это связано с тем что большинство устройств не откалиброваны, а некоторые браузеры не поддерживают цветовые профили <a href="https://en.wikipedia.org/wiki/ICC_profile">устройств вывода</a>.</p>
</div>

<h3 id="Ключевые_цвета">Ключевые цвета</h3>

<p>Ключевые слова для цвета - это идентификаторы без учёта регистра, представляющие определённый цвет, например <code>red</code>, <code>blue</code>, <code>black</code> или <code>lightseagreen</code>. Хотя названия более или менее описывают их соответствующие цвета, они по существу искусственны, без строгого обоснования используемых имён. </p>

<p>Есть несколько предостережений, которые следует учитывать при использовании ключевых слов цвета:</p>

<ul>
 <li><a href="/en-US/docs/Web/HTML">HTML</a> распознает только 16 основных цветовых ключевых слов, найденных в CSS1, используя определённый алгоритм для преобразования нераспознанных значений (часто в совершенно разные цвета). Другие ключевые слова цвета должны использоваться только в CSS и <a href="/en-US/docs/Web/SVG">SVG</a>.</li>
 <li>В отличие от HTML, CSS будет полностью игнорировать неизвестные ключевые слова.</li>
 <li>Ключевые слова цвета все представляют собой простые, сплошные цвета, без прозрачности.</li>
 <li>Несколько ключевых слов являются псевдонимами друг для друга:
  <ul>
   <li><code>aqua</code> / <code>cyan</code></li>
   <li><code>fuchsia</code> / <code>magenta</code></li>
   <li><code>darkgray</code> / <code>darkgrey</code></li>
   <li><code>darkslategray</code> / <code>darkslategrey</code></li>
   <li><code>dimgray</code> / <code>dimgrey</code></li>
   <li><code>lightgray</code> / <code>lightgrey</code></li>
   <li><code>lightslategray</code> / <code>lightslategrey</code></li>
   <li><code>gray</code> / <code>grey</code></li>
   <li><code>slategray</code> / <code>slategrey</code></li>
  </ul>
 </li>
 <li>Хотя многие ключевые слова были адаптированы из <a href="https://en.wikipedia.org/wiki/X_Window_System">X11</a>, их значения RGB могут отличаться от соответствующего цвета в системах X11, поскольку производители иногда адаптируют цвета X11 к своему конкретному оборудованию.</li>
</ul>

<div class="note">
<p><strong>Примечание:</strong> Список принятых ключевых слов претерпел много изменений в ходе эволюции CSS:</p>

<ul>
 <li>CSS Level 1 включал только 16 основных цветов, называемых цветами <a href="https://en.wikipedia.org/wiki/VGA">VGA</a>, поскольку они были взяты из набора отображаемых цветов на видеокартах VGA</li>
 <li>CSS Level 2 добавил ключевое слово <code>orange</code>.</li>
 <li>Хотя различные цвета не в спецификации (в основном адаптированные из списка цветов X11) поддерживались ранними браузерами, они не были формально определены до уровня SVG 1.0 и CSS Colors 3. Они называются расширенными цветовыми <em>ключевыми</em> словами, <em>цветами X11</em> или цветами SVG.</li>
 <li>CSS Colors Level 4 добавил ключевое слово rebeccapurple, <a href="https://codepen.io/trezy/post/honoring-a-great-man">чтобы почтить пионера веб-Эрика Мейера.</a></li>
</ul>
</div>

<table>
 <thead>
  <tr>
   <th scope="col">Спецификация</th>
   <th scope="col">Эквивалент RGB</th>
   <th scope="col">Ключевое слово</th>
   <th scope="col">RGB hex значение</th>
   <th scope="col">Видео сайта</th>
  </tr>
 </thead>
 <tbody>
  <tr style="position: relative;">
   <td rowspan="16">{{SpecName("CSS1")}}</td>
   <td style="background: #000;"></td>
   <td style="text-align: center;"><code>black</code></td>
   <td><code>#000000</code></td>
   <td style="background: black;"></td>
  </tr>
  <tr>
   <td style="background: #C0C0C0;"></td>
   <td style="text-align: center;"><code>silver</code></td>
   <td><code>#c0c0c0</code></td>
   <td style="background: silver;"></td>
  </tr>
  <tr>
   <td style="background: #808080;"></td>
   <td style="text-align: center;"><code>gray</code></td>
   <td><code>#808080</code></td>
   <td style="background: gray;"></td>
  </tr>
  <tr>
   <td style="background: #FFF;"></td>
   <td style="text-align: center;"><code>white</code></td>
   <td><code>#ffffff</code></td>
   <td style="background: white;"></td>
  </tr>
  <tr>
   <td style="background: #800000;"></td>
   <td style="text-align: center;"><code>maroon</code></td>
   <td><code>#800000</code></td>
   <td style="background: maroon;"></td>
  </tr>
  <tr>
   <td style="background: #F00;"></td>
   <td style="text-align: center;"><code>red</code></td>
   <td><code>#ff0000</code></td>
   <td style="background: red;"></td>
  </tr>
  <tr>
   <td style="background: #800080;"></td>
   <td style="text-align: center;"><code>purple</code></td>
   <td><code>#800080</code></td>
   <td style="background: purple;"></td>
  </tr>
  <tr>
   <td style="background: #F0F;"></td>
   <td style="text-align: center;"><code>fuchsia</code></td>
   <td><code>#ff00ff</code></td>
   <td style="background: fuchsia;"></td>
  </tr>
  <tr>
   <td style="background: #008000;"></td>
   <td style="text-align: center;"><code>green</code></td>
   <td><code>#008000</code></td>
   <td style="background: green;"></td>
  </tr>
  <tr>
   <td style="background: #0F0;"></td>
   <td style="text-align: center;"><code>lime</code></td>
   <td><code>#00ff00</code></td>
   <td style="background: lime;"></td>
  </tr>
  <tr>
   <td style="background: #808000;"></td>
   <td style="text-align: center;"><code>olive</code></td>
   <td><code>#808000</code></td>
   <td style="background: olive;"></td>
  </tr>
  <tr>
   <td style="background: #FF0;"></td>
   <td style="text-align: center;"><code>yellow</code></td>
   <td><code>#ffff00</code></td>
   <td style="background: yellow;"></td>
  </tr>
  <tr>
   <td style="background: #000080;"></td>
   <td style="text-align: center;"><code>navy</code></td>
   <td><code>#000080</code></td>
   <td style="background: navy;"></td>
  </tr>
  <tr>
   <td style="background: #00F;"></td>
   <td style="text-align: center;"><code>blue</code></td>
   <td><code>#0000ff</code></td>
   <td style="background: blue;"></td>
  </tr>
  <tr>
   <td style="background: #008080;"></td>
   <td style="text-align: center;"><code>teal</code></td>
   <td><code>#008080</code></td>
   <td style="background: teal;"></td>
  </tr>
  <tr>
   <td style="background: #0FF;"></td>
   <td style="text-align: center;"><code>aqua</code></td>
   <td><code>#00ffff</code></td>
   <td style="background: aqua;"></td>
  </tr>
  <tr>
   <td>{{SpecName("CSS2.1")}}</td>
   <td style="background: #FFA500;"></td>
   <td style="text-align: center;"><code>orange</code></td>
   <td><code>#ffa500</code></td>
   <td style="background: orange;"></td>
  </tr>
  <tr>
   <td rowspan="130">{{SpecName("CSS3 Colors")}}</td>
   <td style="background: #f0f8ff;"></td>
   <td style="text-align: center;"><code>aliceblue</code></td>
   <td><code>#f0f8ff</code></td>
   <td style="background: aliceblue;"></td>
  </tr>
  <tr>
   <td style="background: #faebd7;"></td>
   <td style="text-align: center;"><code>antiquewhite</code></td>
   <td><code>#faebd7</code></td>
   <td style="background: antiquewhite;"></td>
  </tr>
  <tr>
   <td style="background: #7fffd4;"></td>
   <td style="text-align: center;"><code>aquamarine</code></td>
   <td><code>#7fffd4</code></td>
   <td style="background: aquamarine;"></td>
  </tr>
  <tr>
   <td style="background: #f0ffff;"></td>
   <td style="text-align: center;"><code>azure</code></td>
   <td><code>#f0ffff</code></td>
   <td style="background: azure;"></td>
  </tr>
  <tr>
   <td style="background: #f5f5dc;"></td>
   <td style="text-align: center;"><code>beige</code></td>
   <td><code>#f5f5dc</code></td>
   <td style="background: beige;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4c4;"></td>
   <td style="text-align: center;"><code>bisque</code></td>
   <td><code>#ffe4c4</code></td>
   <td style="background: bisque;"></td>
  </tr>
  <tr>
   <td style="background: #ffebcd;"></td>
   <td style="text-align: center;"><code>blanchedalmond</code></td>
   <td><code>#ffebcd</code></td>
   <td style="background: blanchedalmond;"></td>
  </tr>
  <tr>
   <td style="background: #8a2be2;"></td>
   <td style="text-align: center;"><code>blueviolet</code></td>
   <td><code>#8a2be2</code></td>
   <td style="background: blueviolet;"></td>
  </tr>
  <tr>
   <td style="background: #a52a2a;"></td>
   <td style="text-align: center;"><code>brown</code></td>
   <td><code>#a52a2a</code></td>
   <td style="background: brown;"></td>
  </tr>
  <tr>
   <td style="background: #deb887;"></td>
   <td style="text-align: center;"><code>burlywood</code></td>
   <td><code>#deb887</code></td>
   <td style="background: burlywood;"></td>
  </tr>
  <tr>
   <td style="background: #5f9ea0;"></td>
   <td style="text-align: center;"><code>cadetblue</code></td>
   <td><code>#5f9ea0</code></td>
   <td style="background: cadetblue;"></td>
  </tr>
  <tr>
   <td style="background: #7fff00;"></td>
   <td style="text-align: center;"><code>chartreuse</code></td>
   <td><code>#7fff00</code></td>
   <td style="background: chartreuse;"></td>
  </tr>
  <tr>
   <td style="background: #d2691e;"></td>
   <td style="text-align: center;"><code>chocolate</code></td>
   <td><code>#d2691e</code></td>
   <td style="background: chocolate;"></td>
  </tr>
  <tr>
   <td style="background: #ff7f50;"></td>
   <td style="text-align: center;"><code>coral</code></td>
   <td><code>#ff7f50</code></td>
   <td style="background: coral;"></td>
  </tr>
  <tr>
   <td style="background: #6495ed;"></td>
   <td style="text-align: center;"><code>cornflowerblue</code></td>
   <td><code>#6495ed</code></td>
   <td style="background: cornflowerblue;"></td>
  </tr>
  <tr>
   <td style="background: #fff8dc;"></td>
   <td style="text-align: center;"><code>cornsilk</code></td>
   <td><code>#fff8dc</code></td>
   <td style="background: cornsilk;"></td>
  </tr>
  <tr>
   <td style="background: #dc143c;"></td>
   <td style="text-align: center;"><code>crimson</code></td>
   <td><code>#dc143c</code></td>
   <td style="background: crimson;"></td>
  </tr>
  <tr>
   <td style="background: #0ff;"></td>
   <td style="text-align: center;"><code>cyan</code><br>
    (synonym of <code>aqua</code>)</td>
   <td><code>#00ffff</code></td>
   <td style="background: cyan;"></td>
  </tr>
  <tr>
   <td style="background: #00008b;"></td>
   <td style="text-align: center;"><code>darkblue</code></td>
   <td><code>#00008b</code></td>
   <td style="background: darkblue;"></td>
  </tr>
  <tr>
   <td style="background: #008b8b;"></td>
   <td style="text-align: center;"><code>darkcyan</code></td>
   <td><code>#008b8b</code></td>
   <td style="background: darkcyan;"></td>
  </tr>
  <tr>
   <td style="background: #b8860b;"></td>
   <td style="text-align: center;"><code>darkgoldenrod</code></td>
   <td><code>#b8860b</code></td>
   <td style="background: darkgoldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #a9a9a9;"></td>
   <td style="text-align: center;"><code>darkgray</code></td>
   <td><code>#a9a9a9</code></td>
   <td style="background: darkgray;"></td>
  </tr>
  <tr>
   <td style="background: #006400;"></td>
   <td style="text-align: center;"><code>darkgreen</code></td>
   <td><code>#006400</code></td>
   <td style="background: darkgreen;"></td>
  </tr>
  <tr>
   <td style="background: #a9a9a9;"></td>
   <td style="text-align: center;"><code>darkgrey</code></td>
   <td><code>#a9a9a9</code></td>
   <td style="background: darkgrey;"></td>
  </tr>
  <tr>
   <td style="background: #bdb76b;"></td>
   <td style="text-align: center;"><code>darkkhaki</code></td>
   <td><code>#bdb76b</code></td>
   <td style="background: darkkhaki;"></td>
  </tr>
  <tr>
   <td style="background: #8b008b;"></td>
   <td style="text-align: center;"><code>darkmagenta</code></td>
   <td><code>#8b008b</code></td>
   <td style="background: darkmagenta;"></td>
  </tr>
  <tr>
   <td style="background: #556b2f;"></td>
   <td style="text-align: center;"><code>darkolivegreen</code></td>
   <td><code>#556b2f</code></td>
   <td style="background: darkolivegreen;"></td>
  </tr>
  <tr>
   <td style="background: #ff8c00;"></td>
   <td style="text-align: center;"><code>darkorange</code></td>
   <td><code>#ff8c00</code></td>
   <td style="background: darkorange;"></td>
  </tr>
  <tr>
   <td style="background: #9932cc;"></td>
   <td style="text-align: center;"><code>darkorchid</code></td>
   <td><code>#9932cc</code></td>
   <td style="background: darkorchid;"></td>
  </tr>
  <tr>
   <td style="background: #8b0000;"></td>
   <td style="text-align: center;"><code>darkred</code></td>
   <td><code>#8b0000</code></td>
   <td style="background: darkred;"></td>
  </tr>
  <tr>
   <td style="background: #e9967a;"></td>
   <td style="text-align: center;"><code>darksalmon</code></td>
   <td><code>#e9967a</code></td>
   <td style="background: darksalmon;"></td>
  </tr>
  <tr>
   <td style="background: #8fbc8f;"></td>
   <td style="text-align: center;"><code>darkseagreen</code></td>
   <td><code>#8fbc8f</code></td>
   <td style="background: darkseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #483d8b;"></td>
   <td style="text-align: center;"><code>darkslateblue</code></td>
   <td><code>#483d8b</code></td>
   <td style="background: darkslateblue;"></td>
  </tr>
  <tr>
   <td style="background: #2f4f4f;"></td>
   <td style="text-align: center;"><code>darkslategray</code></td>
   <td><code>#2f4f4f</code></td>
   <td style="background: darkslategray;"></td>
  </tr>
  <tr>
   <td style="background: #2f4f4f;"></td>
   <td style="text-align: center;"><code>darkslategrey</code></td>
   <td><code>#2f4f4f</code></td>
   <td style="background: darkslategrey;"></td>
  </tr>
  <tr>
   <td style="background: #00ced1;"></td>
   <td style="text-align: center;"><code>darkturquoise</code></td>
   <td><code>#00ced1</code></td>
   <td style="background: darkturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #9400d3;"></td>
   <td style="text-align: center;"><code>darkviolet</code></td>
   <td><code>#9400d3</code></td>
   <td style="background: darkviolet;"></td>
  </tr>
  <tr>
   <td style="background: #ff1493;"></td>
   <td style="text-align: center;"><code>deeppink</code></td>
   <td><code>#ff1493</code></td>
   <td style="background: deeppink;"></td>
  </tr>
  <tr>
   <td style="background: #00bfff;"></td>
   <td style="text-align: center;"><code>deepskyblue</code></td>
   <td><code>#00bfff</code></td>
   <td style="background: deepskyblue;"></td>
  </tr>
  <tr>
   <td style="background: #696969;"></td>
   <td style="text-align: center;"><code>dimgray</code></td>
   <td><code>#696969</code></td>
   <td style="background: dimgray;"></td>
  </tr>
  <tr>
   <td style="background: #696969;"></td>
   <td style="text-align: center;"><code>dimgrey</code></td>
   <td><code>#696969</code></td>
   <td style="background: dimgrey;"></td>
  </tr>
  <tr>
   <td style="background: #1e90ff;"></td>
   <td style="text-align: center;"><code>dodgerblue</code></td>
   <td><code>#1e90ff</code></td>
   <td style="background: dodgerblue;"></td>
  </tr>
  <tr>
   <td style="background: #b22222;"></td>
   <td style="text-align: center;"><code>firebrick</code></td>
   <td><code>#b22222</code></td>
   <td style="background: firebrick;"></td>
  </tr>
  <tr>
   <td style="background: #fffaf0;"></td>
   <td style="text-align: center;"><code>floralwhite</code></td>
   <td><code>#fffaf0</code></td>
   <td style="background: floralwhite;"></td>
  </tr>
  <tr>
   <td style="background: #228b22;"></td>
   <td style="text-align: center;"><code>forestgreen</code></td>
   <td><code>#228b22</code></td>
   <td style="background: forestgreen;"></td>
  </tr>
  <tr>
   <td style="background: #dcdcdc;"></td>
   <td style="text-align: center;"><code>gainsboro</code></td>
   <td><code>#dcdcdc</code></td>
   <td style="background: gainsboro;"></td>
  </tr>
  <tr>
   <td style="background: #f8f8ff;"></td>
   <td style="text-align: center;"><code>ghostwhite</code></td>
   <td><code>#f8f8ff</code></td>
   <td style="background: ghostwhite;"></td>
  </tr>
  <tr>
   <td style="background: #ffd700;"></td>
   <td style="text-align: center;"><code>gold</code></td>
   <td><code>#ffd700</code></td>
   <td style="background: gold;"></td>
  </tr>
  <tr>
   <td style="background: #daa520;"></td>
   <td style="text-align: center;"><code>goldenrod</code></td>
   <td><code>#daa520</code></td>
   <td style="background: goldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #adff2f;"></td>
   <td style="text-align: center;"><code>greenyellow</code></td>
   <td><code>#adff2f</code></td>
   <td style="background: greenyellow ;"></td>
  </tr>
  <tr>
   <td style="background: #808080;"></td>
   <td style="text-align: center;"><code>grey</code></td>
   <td><code>#808080</code></td>
   <td style="background: grey;"></td>
  </tr>
  <tr>
   <td style="background: #f0fff0;"></td>
   <td style="text-align: center;"><code>honeydew</code></td>
   <td><code>#f0fff0</code></td>
   <td style="background: honeydew;"></td>
  </tr>
  <tr>
   <td style="background: #ff69b4;"></td>
   <td style="text-align: center;"><code>hotpink</code></td>
   <td><code>#ff69b4</code></td>
   <td style="background: hotpink;"></td>
  </tr>
  <tr>
   <td style="background: #cd5c5c;"></td>
   <td style="text-align: center;"><code>indianred</code></td>
   <td><code>#cd5c5c</code></td>
   <td style="background: indianred;"></td>
  </tr>
  <tr>
   <td style="background: #4b0082;"></td>
   <td style="text-align: center;"><code>indigo</code></td>
   <td><code>#4b0082</code></td>
   <td style="background: indigo;"></td>
  </tr>
  <tr>
   <td style="background: #fffff0;"></td>
   <td style="text-align: center;"><code>ivory</code></td>
   <td><code>#fffff0</code></td>
   <td style="background: ivory;"></td>
  </tr>
  <tr>
   <td style="background: #f0e68c;"></td>
   <td style="text-align: center;"><code>khaki</code></td>
   <td><code>#f0e68c</code></td>
   <td style="background: khaki;"></td>
  </tr>
  <tr>
   <td style="background: #e6e6fa;"></td>
   <td style="text-align: center;"><code>lavender</code></td>
   <td><code>#e6e6fa</code></td>
   <td style="background: lavender;"></td>
  </tr>
  <tr>
   <td style="background: #fff0f5;"></td>
   <td style="text-align: center;"><code>lavenderblush</code></td>
   <td><code>#fff0f5</code></td>
   <td style="background: lavenderblush ;"></td>
  </tr>
  <tr>
   <td style="background: #7cfc00;"></td>
   <td style="text-align: center;"><code>lawngreen</code></td>
   <td><code>#7cfc00</code></td>
   <td style="background: lawngreen;"></td>
  </tr>
  <tr>
   <td style="background: #fffacd;"></td>
   <td style="text-align: center;"><code>lemonchiffon</code></td>
   <td><code>#fffacd</code></td>
   <td style="background: lemonchiffon;"></td>
  </tr>
  <tr>
   <td style="background: #add8e6;"></td>
   <td style="text-align: center;"><code>lightblue</code></td>
   <td><code>#add8e6</code></td>
   <td style="background: lightblue;"></td>
  </tr>
  <tr>
   <td style="background: #f08080;"></td>
   <td style="text-align: center;"><code>lightcoral</code></td>
   <td><code>#f08080</code></td>
   <td style="background: lightcoral;"></td>
  </tr>
  <tr>
   <td style="background: #e0ffff;"></td>
   <td style="text-align: center;"><code>lightcyan</code></td>
   <td><code>#e0ffff</code></td>
   <td style="background: lightcyan;"></td>
  </tr>
  <tr>
   <td style="background: #fafad2;"></td>
   <td style="text-align: center;"><code>lightgoldenrodyellow</code></td>
   <td><code>#fafad2</code></td>
   <td style="background: lightgoldenrodyellow ;"></td>
  </tr>
  <tr>
   <td style="background: #d3d3d3;"></td>
   <td style="text-align: center;"><code>lightgray</code></td>
   <td><code>#d3d3d3</code></td>
   <td style="background: lightgray;"></td>
  </tr>
  <tr>
   <td style="background: #90ee90;"></td>
   <td style="text-align: center;"><code>lightgreen</code></td>
   <td><code>#90ee90</code></td>
   <td style="background: lightgreen;"></td>
  </tr>
  <tr>
   <td style="background: #d3d3d3;"></td>
   <td style="text-align: center;"><code>lightgrey</code></td>
   <td><code>#d3d3d3</code></td>
   <td style="background: lightgrey;"></td>
  </tr>
  <tr>
   <td style="background: #ffb6c1;"></td>
   <td style="text-align: center;"><code>lightpink</code></td>
   <td><code>#ffb6c1</code></td>
   <td style="background: lightpink;"></td>
  </tr>
  <tr>
   <td style="background: #ffa07a;"></td>
   <td style="text-align: center;"><code>lightsalmon</code></td>
   <td><code>#ffa07a</code></td>
   <td style="background: lightsalmon;"></td>
  </tr>
  <tr>
   <td style="background: #20b2aa;"></td>
   <td style="text-align: center;"><code>lightseagreen</code></td>
   <td><code>#20b2aa</code></td>
   <td style="background: lightseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #87cefa;"></td>
   <td style="text-align: center;"><code>lightskyblue</code></td>
   <td><code>#87cefa</code></td>
   <td style="background: lightskyblue;"></td>
  </tr>
  <tr>
   <td style="background: #778899;"></td>
   <td style="text-align: center;"><code>lightslategray</code></td>
   <td><code>#778899</code></td>
   <td style="background: lightslategray;"></td>
  </tr>
  <tr>
   <td style="background: #778899;"></td>
   <td style="text-align: center;"><code>lightslategrey</code></td>
   <td><code>#778899</code></td>
   <td style="background: lightslategrey;"></td>
  </tr>
  <tr>
   <td style="background: #b0c4de;"></td>
   <td style="text-align: center;"><code>lightsteelblue</code></td>
   <td><code>#b0c4de</code></td>
   <td style="background: lightsteelblue;"></td>
  </tr>
  <tr>
   <td style="background: #ffffe0;"></td>
   <td style="text-align: center;"><code>lightyellow</code></td>
   <td><code>#ffffe0</code></td>
   <td style="background: lightyellow;"></td>
  </tr>
  <tr>
   <td style="background: #32cd32;"></td>
   <td style="text-align: center;"><code>limegreen</code></td>
   <td><code>#32cd32</code></td>
   <td style="background: limegreen;"></td>
  </tr>
  <tr>
   <td style="background: #faf0e6;"></td>
   <td style="text-align: center;"><code>linen</code></td>
   <td><code>#faf0e6</code></td>
   <td style="background: linen;"></td>
  </tr>
  <tr>
   <td style="background: #ff00ff;"></td>
   <td style="text-align: center;"><code>magenta</code><br>
    (synonym of <code>fuchsia</code>)</td>
   <td><code>#ff00ff</code></td>
   <td style="background: magenta;"></td>
  </tr>
  <tr>
   <td style="background: #66cdaa;"></td>
   <td style="text-align: center;"><code>mediumaquamarine</code></td>
   <td><code>#66cdaa</code></td>
   <td style="background: mediumaquamarine;"></td>
  </tr>
  <tr>
   <td style="background: #0000cd;"></td>
   <td style="text-align: center;"><code>mediumblue</code></td>
   <td><code>#0000cd</code></td>
   <td style="background: mediumblue;"></td>
  </tr>
  <tr>
   <td style="background: #ba55d3;"></td>
   <td style="text-align: center;"><code>mediumorchid</code></td>
   <td><code>#ba55d3</code></td>
   <td style="background: mediumorchid;"></td>
  </tr>
  <tr>
   <td style="background: #9370db;"></td>
   <td style="text-align: center;"><code>mediumpurple</code></td>
   <td><code>#9370db</code></td>
   <td style="background: mediumpurple;"></td>
  </tr>
  <tr>
   <td style="background: #3cb371;"></td>
   <td style="text-align: center;"><code>mediumseagreen</code></td>
   <td><code>#3cb371</code></td>
   <td style="background: mediumseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #7b68ee;"></td>
   <td style="text-align: center;"><code>mediumslateblue</code></td>
   <td><code>#7b68ee</code></td>
   <td style="background: mediumslateblue;"></td>
  </tr>
  <tr>
   <td style="background: #00fa9a;"></td>
   <td style="text-align: center;"><code>mediumspringgreen</code></td>
   <td><code>#00fa9a</code></td>
   <td style="background: mediumspringgreen;"></td>
  </tr>
  <tr>
   <td style="background: #48d1cc;"></td>
   <td style="text-align: center;"><code>mediumturquoise</code></td>
   <td><code>#48d1cc</code></td>
   <td style="background: mediumturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #c71585;"></td>
   <td style="text-align: center;"><code>mediumvioletred</code></td>
   <td><code>#c71585</code></td>
   <td style="background: mediumvioletred;"></td>
  </tr>
  <tr>
   <td style="background: #191970;"></td>
   <td style="text-align: center;"><code>midnightblue</code></td>
   <td><code>#191970</code></td>
   <td style="background: midnightblue;"></td>
  </tr>
  <tr>
   <td style="background: #f5fffa;"></td>
   <td style="text-align: center;"><code>mintcream</code></td>
   <td><code>#f5fffa</code></td>
   <td style="background: mintcream;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4e1;"></td>
   <td style="text-align: center;"><code>mistyrose</code></td>
   <td><code>#ffe4e1</code></td>
   <td style="background: mistyrose;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4b5;"></td>
   <td style="text-align: center;"><code>moccasin</code></td>
   <td><code>#ffe4b5</code></td>
   <td style="background: moccasin;"></td>
  </tr>
  <tr>
   <td style="background: #ffdead;"></td>
   <td style="text-align: center;"><code>navajowhite</code></td>
   <td><code>#ffdead</code></td>
   <td style="background: navajowhite;"></td>
  </tr>
  <tr>
   <td style="background: #fdf5e6;"></td>
   <td style="text-align: center;"><code>oldlace</code></td>
   <td><code>#fdf5e6</code></td>
   <td style="background: oldlace;"></td>
  </tr>
  <tr>
   <td style="background: #6b8e23;"></td>
   <td style="text-align: center;"><code>olivedrab</code></td>
   <td><code>#6b8e23</code></td>
   <td style="background: olivedrab;"></td>
  </tr>
  <tr>
   <td style="background: #ff4500;"></td>
   <td style="text-align: center;"><code>orangered</code></td>
   <td><code>#ff4500</code></td>
   <td style="background: orangered;"></td>
  </tr>
  <tr>
   <td style="background: #da70d6;"></td>
   <td style="text-align: center;"><code>orchid</code></td>
   <td><code>#da70d6</code></td>
   <td style="background: orchid;"></td>
  </tr>
  <tr>
   <td style="background: #eee8aa;"></td>
   <td style="text-align: center;"><code>palegoldenrod</code></td>
   <td><code>#eee8aa</code></td>
   <td style="background: palegoldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #98fb98;"></td>
   <td style="text-align: center;"><code>palegreen</code></td>
   <td><code>#98fb98</code></td>
   <td style="background: palegreen;"></td>
  </tr>
  <tr>
   <td style="background: #afeeee;"></td>
   <td style="text-align: center;"><code>paleturquoise</code></td>
   <td><code>#afeeee</code></td>
   <td style="background: paleturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #db7093;"></td>
   <td style="text-align: center;"><code>palevioletred</code></td>
   <td><code>#db7093</code></td>
   <td style="background: palevioletred;"></td>
  </tr>
  <tr>
   <td style="background: #ffefd5;"></td>
   <td style="text-align: center;"><code>papayawhip</code></td>
   <td><code>#ffefd5</code></td>
   <td style="background: papayawhip;"></td>
  </tr>
  <tr>
   <td style="background: #ffdab9;"></td>
   <td style="text-align: center;"><code>peachpuff</code></td>
   <td><code>#ffdab9</code></td>
   <td style="background: peachpuff;"></td>
  </tr>
  <tr>
   <td style="background: #cd853f;"></td>
   <td style="text-align: center;"><code>peru</code></td>
   <td><code>#cd853f</code></td>
   <td style="background: peru;"></td>
  </tr>
  <tr>
   <td style="background: #ffc0cb;"></td>
   <td style="text-align: center;"><code>pink</code></td>
   <td><code>#ffc0cb</code></td>
   <td style="background: pink;"></td>
  </tr>
  <tr>
   <td style="background: #dda0dd;"></td>
   <td style="text-align: center;"><code>plum</code></td>
   <td><code>#dda0dd</code></td>
   <td style="background: plum;"></td>
  </tr>
  <tr>
   <td style="background: #b0e0e6;"></td>
   <td style="text-align: center;"><code>powderblue</code></td>
   <td><code>#b0e0e6</code></td>
   <td style="background: powderblue;"></td>
  </tr>
  <tr>
   <td style="background: #bc8f8f;"></td>
   <td style="text-align: center;"><code>rosybrown</code></td>
   <td><code>#bc8f8f</code></td>
   <td style="background: rosybrown;"></td>
  </tr>
  <tr>
   <td style="background: #4169e1;"></td>
   <td style="text-align: center;"><code>royalblue</code></td>
   <td><code>#4169e1</code></td>
   <td style="background: royalblue;"></td>
  </tr>
  <tr>
   <td style="background: #8b4513;"></td>
   <td style="text-align: center;"><code>saddlebrown</code></td>
   <td><code>#8b4513</code></td>
   <td style="background: saddlebrown;"></td>
  </tr>
  <tr>
   <td style="background: #fa8072;"></td>
   <td style="text-align: center;"><code>salmon</code></td>
   <td><code>#fa8072</code></td>
   <td style="background: salmon;"></td>
  </tr>
  <tr>
   <td style="background: #f4a460;"></td>
   <td style="text-align: center;"><code>sandybrown</code></td>
   <td><code>#f4a460</code></td>
   <td style="background: sandybrown;"></td>
  </tr>
  <tr>
   <td style="background: #2e8b57;"></td>
   <td style="text-align: center;"><code>seagreen</code></td>
   <td><code>#2e8b57</code></td>
   <td style="background: seagreen;"></td>
  </tr>
  <tr>
   <td style="background: #fff5ee;"></td>
   <td style="text-align: center;"><code>seashell</code></td>
   <td><code>#fff5ee</code></td>
   <td style="background: seashell;"></td>
  </tr>
  <tr>
   <td style="background: #a0522d;"></td>
   <td style="text-align: center;"><code>sienna</code></td>
   <td><code>#a0522d</code></td>
   <td style="background: sienna;"></td>
  </tr>
  <tr>
   <td style="background: #87ceeb;"></td>
   <td style="text-align: center;"><code>skyblue</code></td>
   <td><code>#87ceeb</code></td>
   <td style="background: skyblue;"></td>
  </tr>
  <tr>
   <td style="background: #6a5acd;"></td>
   <td style="text-align: center;"><code>slateblue</code></td>
   <td><code>#6a5acd</code></td>
   <td style="background: slateblue;"></td>
  </tr>
  <tr>
   <td style="background: #708090;"></td>
   <td style="text-align: center;"><code>slategray</code></td>
   <td><code>#708090</code></td>
   <td style="background: slategray;"></td>
  </tr>
  <tr>
   <td style="background: #708090;"></td>
   <td style="text-align: center;"><code>slategrey</code></td>
   <td><code>#708090</code></td>
   <td style="background: slategrey;"></td>
  </tr>
  <tr>
   <td style="background: #fffafa;"></td>
   <td style="text-align: center;"><code>snow</code></td>
   <td><code>#fffafa</code></td>
   <td style="background: snow;"></td>
  </tr>
  <tr>
   <td style="background: #00ff7f;"></td>
   <td style="text-align: center;"><code>springgreen</code></td>
   <td><code>#00ff7f</code></td>
   <td style="background: springgreen;"></td>
  </tr>
  <tr>
   <td style="background: #4682b4;"></td>
   <td style="text-align: center;"><code>steelblue</code></td>
   <td><code>#4682b4</code></td>
   <td style="background: steelblue;"></td>
  </tr>
  <tr>
   <td style="background: #d2b48c;"></td>
   <td style="text-align: center;"><code>tan</code></td>
   <td><code>#d2b48c</code></td>
   <td style="background: tan;"></td>
  </tr>
  <tr>
   <td style="background: #d8bfd8;"></td>
   <td style="text-align: center;"><code>thistle</code></td>
   <td><code>#d8bfd8</code></td>
   <td style="background: thistle;"></td>
  </tr>
  <tr>
   <td style="background: #ff6347;"></td>
   <td style="text-align: center;"><code>tomato</code></td>
   <td><code>#ff6347</code></td>
   <td style="background: tomato;"></td>
  </tr>
  <tr>
   <td style="background: #40e0d0;"></td>
   <td style="text-align: center;"><code>turquoise</code></td>
   <td><code>#40e0d0</code></td>
   <td style="background: turquoise;"></td>
  </tr>
  <tr>
   <td style="background: #ee82ee;"></td>
   <td style="text-align: center;"><code>violet</code></td>
   <td><code>#ee82ee</code></td>
   <td style="background: violet;"></td>
  </tr>
  <tr>
   <td style="background: #f5deb3;"></td>
   <td style="text-align: center;"><code>wheat</code></td>
   <td><code>#f5deb3</code></td>
   <td style="background: wheat;"></td>
  </tr>
  <tr>
   <td style="background: #f5f5f5;"></td>
   <td style="text-align: center;"><code>whitesmoke</code></td>
   <td><code>#f5f5f5</code></td>
   <td style="background: whitesmoke;"></td>
  </tr>
  <tr>
   <td style="background: #9acd32;"></td>
   <td style="text-align: center;"><code>yellowgreen</code></td>
   <td><code>#9acd32</code></td>
   <td style="background: yellowgreen;"></td>
  </tr>
  <tr>
   <td>{{SpecName("CSS4 Colors")}}</td>
   <td style="background: #639;"></td>
   <td style="text-align: center;"><a href="https://en.wikipedia.org/wiki/Eric_A._Meyer#Personal_life"><code>rebeccapurple</code></a></td>
   <td><code>#663399</code></td>
   <td style="background: rebeccapurple;"></td>
  </tr>
 </tbody>
</table>

<h3 id="Прозрачное_ключевое_слово"><code><a>Прозрачное</a></code> ключевое слово</h3>

<p>Ключевое слово <code>transparent</code> представляет собой полностью прозрачный цвет. Это делает фон позади цветного элемента полностью видимым. Технически <code>transparent </code>- это ярлык для <code>rgba (0,0,0,0)</code>.</p>

<div class="note">
<p><strong>Примечание по совместимости:</strong> чтобы предотвратить непредвиденное поведение, например, в {{cssxref ("градиент")}}, текущая спецификация CSS утверждает, что <code>transparent</code> должен быть вычислен в <a href="https://www.w3.org/TR/2012/CR-css3-images-20120417/#color-stop-syntax">Альфа-предварительно умноженном цветовом пространстве</a>. Однако имейте в виду, что старые браузеры могут рассматривать его как чёрный с Альфа-значением <code>0</code>.</p>
</div>

<div class="note">
<p><strong>Историческая запись:</strong> <code>transparent</code> не был истинным цветом на уровне CSS 2 (Редакция 1). Это было специальное ключевое слово, которое можно было использовать вместо обычного значения <code>&lt;color&gt;</code> для двух свойств CSS: {{Cssxref("background")}} и {{Cssxref("border")}}. Он был существенно добавлен, чтобы позволить разработчикам переопределить унаследованный сплошной цвет. С появлением Альфа-каналов в CSS Colors Level 3, <code>transparent </code>был переопределён как истинный цвет. Теперь его можно использовать везде, где можно использовать значение <code>&lt;color&gt;</code>.</p>
</div>

<h3 id="currentColor_ключевое_слово"><code><a id="currentColor">currentColor</a></code> ключевое слово</h3>

<p>Ключевое слово <code>currentColor</code> представляет значение свойства элемента {{Cssxref("color")}}. Это позволяет использовать значение <code>color</code> для свойств, которые не получают его по умолчанию.</p>

<p>Если текущий цвет используется в качестве значения свойства <code>color</code> , он вместо этого принимает его значение из наследуемого значения свойства <code>color</code>.</p>

<h4 id="currentColor_пример">currentColor пример</h4>

<pre class="brush: html">&lt;div style="color:blue; border: 1px dashed currentColor;"&gt;
  Цвет текста-синий.
  &lt;div style="background:currentColor; height:9px;"&gt;&lt;/div&gt;
  This block is surrounded by a blue border.
&lt;/div&gt;</pre>

<p>{{EmbedLiveSample("currentColor_пример")}}</p>

<h3 id="RGB_цвет">RGB цвет</h3>

<p>Цветовая модель RGB определяет заданный цвет в соответствии с его красными, зелёными и синими компонентами. Дополнительный Альфа-компонент представляет прозрачность цвета.</p>

<h4 id="Синтаксис">Синтаксис</h4>

<p>Цвета RGB могут быть выражены как шестнадцатеричными (с префиксом #), так и функциональными (<code>rgb ()</code>, <code>rgba ()</code>) нотациями.</p>

<div class="note">
<p><strong>Примечание:</strong> начиная с уровня цветов CSS 4,<code> rgba()</code> является псевдонимом для <code>rgb()</code>. В браузерах, реализующих стандарт уровня 4, они принимают одни и те же параметры и ведут себя одинаково.</p>
</div>

<dl>
 <dt>Шестнадцатеричное представление: <code>#RRGGBB[AA]</code></dt>
 <dd><code>R</code> (red), <code>G</code> (green), <code>B</code> (blue), and <code>A</code> (alpha) are hexadecimal characters (0-9, A-F). <code>A</code> is optional. For example, <code>#ff0000</code> is equivalent to <code>#ff0000ff</code>. <code>R</code> (красный), G (зелёный), B (синий) и A (Альфа) являются шестнадцатеричными символами (0-9, A-F). Это не является обязательным. Например, <code>#ff0000</code> эквивалентно<code> #ff0000ff</code>.</dd>
 <dt>Шестнадцатеричное представление: <code>#RGB[A]</code></dt>
 <dd><code>R</code> (красный), <code>G</code> (зелёный), <code>B</code> (синий) и <code>A</code> (Альфа) являются шестнадцатеричными символами (0-9, A-F). Это не является обязательным. Трёхзначная нотация (<code>#RGB</code>) является более короткой версией шестизначной формы (<code>#RRGGBB</code>). Например, <code>#f09</code> имеет тот же цвет, что и <code>#ff0099</code>. Кроме того, четырёхзначная нотация RGB (<code>#RGB</code>) является более короткой версией восьмизначной формы (<code>#RRGGBBAA</code>). Например, #0f38 имеет тот же цвет, что и <code>#00ff3388</code>.</dd>
 <dt>Функциональная нотация: <code>rgb(R, G, B[, A])</code> или <code>rgba(R, G, B, A)</code></dt>
 <dd><code>R</code> (красный), <code>G </code>(зелёный) и <code>B</code> (синий) могут быть либо {{cssxref("&lt;number&gt;")}}s, либо {{cssxref("&lt;percentage&gt;")}}s, где число <code>255 </code>соответствует <code>100%</code>. А (Альфа) может быть {{cssxref("&lt;number&gt;")}} между <code>0</code> и <code>1</code> или {{cssxref("&lt;percentage&gt;")}}, где число 1 соответствует <code>100%</code> (полная непрозрачность).</dd>
 <dt>Функциональная нотация: <code>rgb(R G B[ A])</code> or <code>rgba(R G B A)</code></dt>
 <dd>CSS Colors Level 4 добавляет поддержку разделённых пробелами значений в функциональной нотации.</dd>
</dl>

<h4 id="Пример">Пример</h4>

<h5 id="RGB_варианты_синтаксиса">RGB варианты синтаксиса</h5>

<p>В этом примере показано множество способов создания одного цвета с помощью различных цветовых синтаксисов RGB.</p>

<pre>/* Все эти варианты синтаксиса задают один и тот же цвет: полностью непрозрачный ярко-розовый. */

/* Шестнадцатеричный синтаксис */
#f09
#F09
#ff0099
#FF0099

/* Функциональный синтаксис */
rgb(255,0,153)
rgb(255, 0, 153)
rgb(255, 0, 153.0)
rgb(100%,0%,60%)
rgb(100%, 0%, 60%)
rgb(100%, 0, 60%) /* Ошибка! Не смешивайте цифры и проценты. */
rgb(255 0 153)

/* Шестнадцатеричный синтаксис с Альфа-значением */
#f09f
#F09F
#ff0099ff
#FF0099FF

/* Функциональный синтаксис с Альфа-значением */
rgb(255, 0, 153, 1)
rgb(255, 0, 153, 100%)

/* Синтаксис пробелов */
rgb(255 0 153 / 1)
rgb(255 0 153 / 100%)

/* Функциональный синтаксис со значением floats */
rgb(255, 0, 153.6, 1)
rgb(1e2, .5e1, .5e0, +.25e2%)
</pre>

<h5 id="RGB_вариации_прозрачности">RGB вариации прозрачности</h5>

<pre>/* Шестнадцатеричный синтаксис */
#3a30                   <span style="background: #3a30;"> /*   0% непрозрачный зелёный цвет */ </span>
#3A3F                   <span style="background: #3A3F;"> /* полный непрозрачный зелёный цвет */ </span>
#33aa3300               <span style="background: #33aa3300;"> /*   0% непрозрачный зелёный цвет */ </span>
#33AA3380               <span style="background: #33AA3380;"> /* 50% непрозрачный зелёный цвет */ </span>

/* Функциональный синтаксис */
rgba(51, 170, 51, .1)   <span style="background: rgba(51, 170, 51, .1);"> /* непрозрачный зелёный цвет на 10%  */ </span>
rgba(51, 170, 51, .4)   <span style="background: rgba(51, 170, 51, .4);"> /* непрозрачный зелёный цвет на */ </span>
rgba(51, 170, 51, .7)   <span style="background: rgba(51, 170, 51, .7);"> /* непрозрачный зелёный цвет на 70% */ </span>
rgba(51, 170, 51,  1)   <span style="background: rgba(51, 170, 51,  1);"> /* полный непрозрачный зелёный цвет  */ </span>

/* Синтаксис пробелов */
rgba(51 170 51 / 0.4)   <span> /* непрозрачный зелёный цвет  на 40%*/ </span>
rgba(51 170 51 / 40%)   <span> /* непрозрачный зелёный цвет на 40% */

</span>/* Функциональный синтаксис со значением floats */
rgba(255, 0, 153.6, 1)
rgba(1e2, .5e1, .5e0, +.25e2%)
</pre>

<h3 id="Цвет_HSL">Цвет HSL </h3>

<p>Цветовая модель HSL определяет заданный цвет в соответствии с его компонентами оттенка, насыщенности и яркости. Дополнительный Альфа-компонент представляет прозрачность цвета.</p>

<p>Многие дизайнеры считают HSL более интуитивным, чем RGB, поскольку он позволяет независимо регулировать оттенок, насыщенность и лёгкость. HSL также может упростить создание набора подходящих цветов (например, когда вы хотите несколько оттенков одного оттенка).</p>

<h4 id="Синтаксис_2">Синтаксис</h4>

<p>Цвета HSL выражаются через функциональные обозначения <code>hsl()</code> и <code>hsla()</code>.</p>

<div class="note">
<p><strong>Примечание</strong>:  Начиная с уровня цветов CSS 4, <code>hsla()</code> является псевдонимом для <code>hsl()</code>. В браузерах, реализующих стандарт уровня 4, они принимают одни и те же параметры и ведут себя одинаково.</p>
</div>

<dl>
 <dt>Функциональная нотация: <code>hsl(H, S, L[, A])</code> или<code>hsla(H, S, L, A)</code></dt>
 <dd><p><code>H</code>  (hue) - это {{cssxref("&lt;угол&gt;")}} цветового круга, заданного в <code>deg</code>S, <code>rad</code>s, градусах или поворотах {{SpecName("CSS4 Colors","#The-HSL-notation")}}. При записи в виде unitless {{cssxref ("&lt;number&gt;")}} он интерпретируется как Градусы, как указано в {{SpecName ("CSS3 Colors","#hsl-color")}}. По определению, red=<code>0</code> deg=<code>360</code> град, с другими цветами, распространёнными по кругу, поэтому green=120deg град, blue=240deg град и т. д. В качестве &lt; угла &gt; он неявно обёртывается таким образом, что -120deg=240deg, 480deg=120deg, -1turn=1turn, и т. д.</p>
 <p><code>S</code> (<code>насыщенность</code>) и <code>L</code> (<code>лёгкость</code>) являются процентами. <code>100%</code> насыщенность полностью насыщена, в то время как 0% полностью ненасыщен (серый). <code>100%</code> лёгкость белый, <code>0%</code> лёгкость чёрный, и <code>50%</code> лёгкость “<code>нормально</code>.”</p>
 <p><code>A</code> (alpha) can be a {{cssxref("&lt;number&gt;")}} between <code>0</code> and <code>1</code>, or a {{cssxref("&lt;percentage&gt;")}}, where the number <code>1</code> corresponds to <code>100%</code> (full opacity). <code>A</code> (Альфа) может быть {{cssxref("&lt;number&gt;")}} между <code>0</code> и <code>1</code> или {{cssxref("&lt;percentage&gt;")}}, где число <code>1</code> соответствует <code>100%</code> (полная непрозрачность).</p></dd>
 <dt>Функциональная нотация: <code>hsl(H S L[ A])</code> or <code>hsla(H S L A)</code></dt>
 <dd>CSS Colors Level 4 добавляет поддержку разделённых пробелами значений в функциональной нотации.</dd>
</dl>

<h4 id="Examples">Examples</h4>

<h5 id="HSL_варианты_синтаксиса">HSL варианты синтаксиса</h5>

<pre>/* Все эти примеры указывают один и тот же цвет: лаванда. */
hsl(270,60%,70%)
hsl(270, 60%, 70%)
hsl(270 60% 70%)
hsl(270deg, 60%, 70%)
hsl(4.71239rad, 60%, 70%)
hsl(.75turn, 60%, 70%)

/* Все эти примеры указывают один и тот же цвет: лаванда, которая на 15% непрозрачна. */
hsl(270, 60%, 50%, .15)
hsl(270, 60%, 50%, 15%)
hsl(270 60% 50% / .15)
hsl(270 60% 50% / 15%)
</pre>

<h5 id="Полностью_насыщенные_цвета">Полностью насыщенные цвета</h5>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Нотация</th>
   <th scope="col">Описание:</th>
   <th scope="col">Итог</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>hsl(0, 100%, 50%)</code></td>
   <td>red</td>
   <td style="background: hsl(0,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(30, 100%, 50%)</code></td>
   <td>orange</td>
   <td style="background: hsl(30,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(60, 100%, 50%)</code></td>
   <td>yellow</td>
   <td style="background: hsl(60,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(90, 100%, 50%)</code></td>
   <td>lime green</td>
   <td style="background: hsl(90,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 50%)</code></td>
   <td>green</td>
   <td style="background: hsl(120,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(150, 100%, 50%)</code></td>
   <td>blue-green</td>
   <td style="background: hsl(150,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(180, 100%, 50%)</code></td>
   <td>cyan</td>
   <td style="background: hsl(180,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(210, 100%, 50%)</code></td>
   <td>sky blue</td>
   <td style="background: hsl(210,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(240, 100%, 50%)</code></td>
   <td>blue</td>
   <td style="background: hsl(240,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(270, 100%, 50%)</code></td>
   <td>purple</td>
   <td style="background: hsl(270,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(300, 100%, 50%)</code></td>
   <td>magenta</td>
   <td style="background: hsl(300,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(330, 100%, 50%)</code></td>
   <td>pink</td>
   <td style="background: hsl(330,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(360, 100%, 50%)</code></td>
   <td>red</td>
   <td style="background: hsl(360,100%,50%);"></td>
  </tr>
 </tbody>
</table>

<h5 id="Более_светлая_и_более_тёмная_зелень">Более светлая и более тёмная зелень</h5>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Нотация</th>
   <th scope="col">Описание:</th>
   <th scope="col">Итог</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>hsl(120, 100%, 0%)</code></td>
   <td>black</td>
   <td style="background: hsl(120,100%,0%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 20%)</code></td>
   <td></td>
   <td style="background: hsl(120,100%,20%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 40%)</code></td>
   <td></td>
   <td style="background: hsl(120,100%,40%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 60%)</code></td>
   <td></td>
   <td style="background: hsl(120,100%,60%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 80%)</code></td>
   <td></td>
   <td style="background: hsl(120,100%,80%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 100%, 100%)</code></td>
   <td>white</td>
   <td style="background: hsl(120,100%,100%);"></td>
  </tr>
 </tbody>
</table>

<h5 id="Насыщенная_и_ненасыщенная_зелень">Насыщенная и ненасыщенная зелень</h5>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Нотация</th>
   <th scope="col">Описание:</th>
   <th scope="col">Итог</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>hsl(120, 100%, 50%)</code></td>
   <td>green</td>
   <td style="background: hsl(120,100%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 80%, 50%)</code></td>
   <td></td>
   <td style="background: hsl(120,80%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 60%, 50%)</code></td>
   <td></td>
   <td style="background: hsl(120,60%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 40%, 50%)</code></td>
   <td></td>
   <td style="background: hsl(120,40%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 20%, 50%)</code></td>
   <td></td>
   <td style="background: hsl(120,20%,50%);"></td>
  </tr>
  <tr>
   <td><code>hsl(120, 0%, 50%)</code></td>
   <td>gray</td>
   <td style="background: hsl(120,0%,50%);"></td>
  </tr>
 </tbody>
</table>

<h5 id="Вариации_прозрачности_HSL">Вариации прозрачности HSL</h5>

<pre>hsla(240, 100%, 50%, .05)    <span style="background: hsla(240,100%,50%,0.05);"> /* непрозрачный синий на 5% */ </span>
hsla(240, 100%, 50%, .4)     <span style="background: hsla(240,100%,50%,0.4);"> /* непрозрачный синий на 40% */ </span>
hsla(240, 100%, 50%, .7)     <span style="background: hsla(240,100%,50%,0.7);"> /* непрозрачный синий на 70% */ </span>
hsla(240, 100%, 50%, 1)      <span style="background: hsla(240,100%,50%,1);"> /* полный непрозрачный синий */ </span>

/* Синтаксис пробелов */
hsla(240 100% 50% / .05)     <span style="background: hsla(240,100%,50%,0.05);"> /* непрозрачный синий на  5% */ </span>

/* Процентное значение для Альфа */
hsla(240 100% 50% / 5%)      <span style="background: hsla(240,100%,50%,0.05);"> /*  непрозрачный синий на 5% */ </span>
</pre>

<h3 id="Системный_цвет">Системный цвет</h3>

<p>Не все системные цвета поддерживаются на всех системах. {{deprecated_inline}} для использования на общедоступных веб-страницах.</p>

<dl>
 <dt>ActiveBorder</dt>
 <dd>Активная граница окна.</dd>
 <dt>ActiveCaption</dt>
 <dd>Активный заголовок окна. Должен использоваться с текстом <code>CaptionText</code> в качестве цвета переднего плана.</dd>
 <dt>AppWorkspace</dt>
 <dd>Цвет фона интерфейса нескольких документов.</dd>
 <dt>Background</dt>
 <dd>Фон рабочего стола.</dd>
 <dt>ButtonFace</dt>
 <dd>Цвет фона лица для трёхмерных элементов, которые появляются 3-D из-за одного слоя окружающей границы. Следует использовать с текстом <code>ButtonText</code> цвет переднего плана.</dd>
 <dt>ButtonHighlight</dt>
 <dd>Цвет границы, обращённой к источнику света для 3-D элементов, которые появляются 3-D из-за этого слоя окружающей границы.</dd>
 <dt>ButtonShadow</dt>
 <dd>Цвет границы вдали от источника света для 3-D элементов, которые появляются 3-D из-за этого слоя окружающей границы. Цвет границы находится вдали от источника света для трёхмерных элементов, которые появляются 3-D из-за этого слоя, окружающего границу.</dd>
 <dt>ButtonText</dt>
 <dd>Следует использовать с <code>ButtonFace</code> или <code>ThreeDFace</code> цвет фона.</dd>
 <dt>CaptionText</dt>
 <dd>Текст в заголовке, поле размера и поле со стрелкой прокрутки. Следует использовать с цветом фона <code>ActiveCaption</code>.</dd>
 <dt>GrayText</dt>
 <dd>Серый (отключён) текст.</dd>
 <dt>Highlight</dt>
 <dd>Элемент(ы), выбранный в элементе управления. Следует использовать с <code>HighlightText</code> текста цветом переднего плана.</dd>
 <dt>HighlightText</dt>
 <dd>Текст элемента(ов), выбранного в элементе управления. Следует использовать с подсветкой цвета фона.</dd>
 <dt>InactiveBorder</dt>
 <dd>Граница неактивного окна.</dd>
 <dt>InactiveCaption</dt>
 <dd>Заголовок неактивного окна. Должен использоваться с цветом переднего плана <code>InactiveCaptionText</code>.</dd>
 <dt>InactiveCaptionText</dt>
 <dd>Следует использовать с <code>InactiveCaption</code> неактивным цветом фона заголовка.</dd>
 <dt>InfoBackground</dt>
 <dd>Цвет фона для элементов управления всплывающей подсказки. Должен использоваться с цветом переднего плана <code>InfoText</code>.</dd>
 <dt>InfoText</dt>
 <dd>Цвет текста элементов подсказки. Должен использоваться с и<code>InfoBackground</code>фона.</dd>
 <dt>Menu</dt>
 <dd>Фон меню. Должен использоваться с <code>MenuText</code> или<code>-moz-MenuBarText</code>строки меню цвет переднего плана.</dd>
 <dt>MenuText</dt>
 <dd>Текст в меню. Следует использовать с меню Цвет фона.</dd>
 <dt>Scrollbar</dt>
 <dd>Цвет фона полос прокрутки.</dd>
 <dt>ThreeDDarkShadow</dt>
 <dd>Цвет более тёмной (как правило, внешней) из двух границ от источника света для трёхмерных элементов, которые появляются 3-D из-за двух концентрических слоёв окружающей границы.</dd>
 <dt>ThreeDFace</dt>
 <dd>Should be used with the <code>ButtonText</code> foreground color. Цвет фона лица для трёхмерных элементов, которые появляются 3-D из-за двух концентрических слоёв окружающей границы. Следует использовать с текстом кнопки цвет переднего плана.</dd>
 <dt>ThreeDHighlight</dt>
 <dd>Цвет более светлого (обычно внешнего) из двух границ, обращённых к источнику света для 3-D элементов, которые появляются 3-D из-за двух концентрических слоёв окружающей границы.</dd>
 <dt>ThreeDLightShadow</dt>
 <dd>Цвет более тёмной (обычно внутренней) из двух границ, обращённых к источнику света для 3-D элементов, которые появляются 3-D из-за двух концентрических слоёв окружающей границы.</dd>
 <dt>ThreeDShadow</dt>
 <dd>Цвет более светлого (как правило, внутреннего) из двух границ от источника света для 3-D элементов, которые появляются 3-D из-за двух концентрических слоёв окружающей границы.</dd>
 <dt>Window</dt>
 <dd>Фон окна. Следует использовать с <code>WindowText</code> цвет переднего плана.</dd>
 <dt>WindowFrame</dt>
 <dd>Оконная рама</dd>
 <dt>WindowText</dt>
 <dd>Текст в windows. Следует использовать с цветом фона окна.</dd>
</dl>

<h3 id="Расширенные_Цвета_Системы_Mozilla">Расширенные Цвета Системы Mozilla</h3>

<dl>
 <dt>-moz-ButtonDefault</dt>
 <dd>Цвет границы вокруг кнопки, которые обозначают действие по умолчанию для диалогового окна.</dd>
 <dt>-moz-ButtonHoverFace</dt>
 <dd>Цвет фона кнопки, на которую наведён указатель мыши (который будет Трёхлинейным или лицом кнопки, когда указатель мыши не находится над ним). Следует использовать с-moz-кнопка наведения текста цвет переднего плана.</dd>
 <dt>-moz-ButtonHoverText</dt>
 <dd>Цвет текста кнопки, на которую наведён указатель мыши (который будет ButtonText, когда указатель мыши не находится над ним). Следует использовать с-<code>-moz-ButtonHoverFace background</code> color.</dd>
 <dt>-moz-CellHighlight</dt>
 <dd>Цвет фона для выбранного элемента в виджете дерево. Следует использовать с цветом переднего плана <code>-moz-CellHighlightText</code>. Смотрите также<code>-moz-html-CellHighlight</code>.</dd>
 <dt>-moz-CellHighlightText</dt>
 <dd>Цвет текста для выбранного элемента в дереве. Следует использовать с цветом фона <code>moz-CellHighlight background</code>. Смотрите также <code>-moz-html-CellHighlightText</code> выделения ячейки.</dd>
 <dt>-moz-Combobox</dt>
 <dd> {{Gecko_minversion_inline ("1.9.2")}} цвет фона для комбинированных полей <code>-moz-ComboboxText</code>. Должен использоваться с цветом переднего плана текста-moz-Combobox. В версиях до 1.9.2 вместо этого используйте <code>-moz-Field</code>.</dd>
 <dt>-moz-ComboboxText</dt>
 <dd>{Gecko_minversion_inline ("1.9.2")}} цвет текста для комбинированных полей. Следует использовать с цветом фона <code>-moz-Combobox</code>. В версиях до 1.9.2 вместо этого используйте <code>-moz-FieldText</code>.</dd>
 <dt>-moz-Dialog</dt>
 <dd>Цвет фона для диалоговых окон. Должен использоваться с цветом переднего плана -<code>-moz-DialogText</code>.</dd>
 <dt>-moz-DialogText</dt>
 <dd>Цвет текста для диалоговых окон. Должен использоваться с цветом фона <code>-moz-Dialog</code>.</dd>
 <dt>-moz-dragtargetzone</dt>
 <dt>-moz-EvenTreeRow</dt>
 <dd>{{gecko_minversion_inline("1.9")}} цвет фона для чётных строк в дереве. Должен использоваться с цветом переднего плана <code>-moz-FieldText</code>. В версиях Gecko до 1.9, используйте-moz-поле. Смотрите также <code>-moz-OddTreeRow</code>.</dd>
 <dt>-moz-Field</dt>
 <dd>Text field background color. Should be used with the <code>-moz-FieldText</code> foreground color. Цвет фона текстового поля. Должен использоваться с цветом переднего плана<code>-moz-FieldText</code>.</dd>
 <dt>-moz-FieldText</dt>
 <dd>Text field text color. Should be used with the <code>-moz-Field</code>, <code>-moz-EvenTreeRow</code>, or <code>-moz-OddTreeRow</code> background color. Текстовое поле цвет текста. Следует использовать с <code>-moz-Field</code>, <code>-moz-EvenTreeRow</code> или <code>-moz-OddTreeRow</code> цветом фона строки дерева.</dd>
 <dt>-moz-html-CellHighlight</dt>
 <dd>{{gecko_minversion_inline("1.9")}} Background color for highlighted item in HTML {{HTMLElement("select")}}s. Should be used with the <code>-moz-html-CellHighlightText</code> foreground color. Prior to Gecko 1.9, use <code>-moz-CellHighlight</code>. {{gecko_minversion_inline ("1.9")}} цвет фона для выделенного элемента в HTML {{HTMLElement ("select")}} s. должен использоваться с цветом переднего плана <code>-moz-html-CellHighlight</code>. До Gecko 1.9, используйте <code>-moz-CellHighlightText</code>.                                    </dd>
 <dt>-moz-html-CellHighlightText</dt>
 <dd>{{gecko_minversion_inline ("1.9")}} цвет текста для  <code>-moz-html-CellHighlight </code>выделенных элементов в HTML {{HTMLElement ("select")}} s. должен использоваться с цветом фона. До Gecko 1.9, используйте <code>moz-html-CellHighlight</code>.</dd>
 <dt>-moz-mac-accentdarkestshadow</dt>
 <dt>-moz-mac-accentdarkshadow</dt>
 <dt>-moz-mac-accentface</dt>
 <dt>-moz-mac-accentlightesthighlight</dt>
 <dt>-moz-mac-accentlightshadow</dt>
 <dt>-moz-mac-accentregularhighlight</dt>
 <dt>-moz-mac-accentregularshadow</dt>
 <dt>-moz-mac-chrome-active</dt>
 <dd>{{Gecko_minversion_inline("1.9.1")}}</dd>
 <dt>-moz-mac-chrome-inactive</dt>
 <dd>{{Gecko_minversion_inline("1.9.1")}}</dd>
 <dt>-moz-mac-focusring</dt>
 <dt>-moz-mac-menuselect</dt>
 <dt>-moz-mac-menushadow</dt>
 <dt>-moz-mac-menutextselect</dt>
 <dt>-moz-MenuHover</dt>
 <dd>Цвет фона для зависших пунктов меню. Часто похожи на <code>Highlight</code>. Следует использовать с <code>moz-MenuHoverText </code>или <code>-moz-MenuBarHoverText</code> при наведении цвет текста переднего плана.</dd>
 <dt>-moz-MenuHoverText</dt>
 <dd>Text color for hovered menu items. Often similar to <code>HighlightText</code>. Should be used with the <code>-moz-MenuHover</code> background color. Цвет текста для зависших пунктов меню. Часто похоже на выделение текста <code>HighlightText</code>. Следует использовать  с <code>-moz-MenuHover</code> наведите цвет фона.</dd>
 <dt>-moz-MenuBarText</dt>
 <dd>{{Gecko_minversion_inline ("1.9.2")}} цвет текста в строках меню. Часто похоже на текст меню  "<code>MenuText</code>". Должен использоваться поверх фона <code>Menu</code>.</dd>
 <dt>-moz-MenuBarHoverText</dt>
 <dd>Цвет для зависшего текста в строках меню. Часто похоже на <code>-moz-MenuHoverText</code>меню наведения текста. Следует использовать поверх <code>-moz-MenuHover</code> наведите фон.</dd>
 <dt>-moz-nativehyperlinktext</dt>
 <dd>{{Gecko_minversion_inline ("1.9.1")}} цвет гиперссылки платформы по умолчанию.</dd>
 <dt>-moz-OddTreeRow</dt>
 <dd>{{gecko_minversion_inline("1.9")}} цвет фона для нечётных строк в дереве. Должен использоваться с цветом переднего плана <code>-moz-FieldText</code>. В версиях Gecko до 1.9, используйте <code>-moz-Field</code>. Смотрите также <code>-moz-EvenTreeRow</code>.</dd>
 <dt>-moz-win-communicationstext</dt>
 <dd>{{gecko_minversion_inline ("1.9")}} следует использовать для текста в объектах с <code>{{cssxref ("- moz-appearance")}}:- moz-win-communications-toolbox;</code>.</dd>
 <dt>-moz-win-mediatext</dt>
 <dd>{{gecko_minversion_inline ("1.9")}} следует использовать для текста в объектах с <code>{{cssxref ("- moz-appearance")}}:- moz-win-media-toolbox</code>.</dd>
 <dt>-moz-win-accentcolor</dt>
 <dd>{{gecko_minversion_inline ("56")}}<br>
 Используется для доступа к пользовательскому цвету акцента Windows 10, который можно установить в меню Пуск, панели задач, заголовках и т. д.</dd>
 <dt>-moz-win-accentcolortext</dt>
 <dd>{{gecko_minversion_inline ("56")}}<br>
 Используется для доступа к цвету текста, размещённого над цветом пользовательского акцента Windows 10 в меню Пуск, панели задач, заголовках и т. д.</dd>
</dl>

<h3 id="Расширения_Цветовых_Предпочтений_Mozilla">Расширения Цветовых Предпочтений Mozilla</h3>

<dl style="font: small Tahoma,'Liberation Sans','Nimbus Sans L',sans-serif; border: 1px solid powderblue; padding: 0.5em 0 0.5em 0.5em; background: #eee;">
 <dt>-moz-activehyperlinktext</dt>
 <dd>Пользовательское предпочтение цвета текста активных ссылок. Должен использоваться с цветом фона документа по умолчанию.</dd>
 <dt>-moz-default-background-color</dt>
 <dd>{{Gecko_minversion_inline ("5.0")}} предпочтения пользователя для цвета фона документа.</dd>
 <dt>-moz-default-color</dt>
 <dd>{{Gecko_minversion_inline ("5.0")}} предпочтения пользователя для цвета текста.</dd>
 <dt>-moz-hyperlinktext</dt>
 <dd>Предпочтения пользователя для цвета текста непрошеных ссылок. Должен использоваться с цветом фона документа по умолчанию.</dd>
 <dt>-moz-visitedhyperlinktext</dt>
 <dd>Предпочтения пользователя для цвета текста посещённых ссылок. Должен использоваться с цветом фона документа по умолчанию.</dd>
</dl>

<h2 id="Интерполяция">Интерполяция</h2>

<p>В анимации и <a href="/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients">градиентах </a>значения <code>&lt;color&gt;</code> интерполируются на каждый из их <a href="https://www.gimp.org/docs/plug-in/appendix-alpha.html">красных, зелёных и синих компонентов</a>. Каждый компонент интерполируется как реальное число с плавающей запятой. Обратите внимание, что интерполяция цветов происходит в Альфа-предварительно умноженном цветовом пространстве rgba, чтобы предотвратить появление неожиданных серых цветов. В анимации, скорость интерполяции определяется <a href="/en-US/docs/Web/CSS/single-transition-timing-function">функцией времени</a>.</p>

<h2 id="Соображения_доступности">Соображения доступности</h2>

<p>Некоторые люди с трудом различают цвета. Рекомендация <a href="https://www.w3.org/TR/WCAG/#visual-audio-contrast">WCAG 2.0</a> настоятельно рекомендует не использовать цвет в качестве единственного средства передачи определённого сообщения, действия или результата. Дополнительную информацию см. В <a href="/en-US/docs/Learn/Accessibility/CSS_and_JavaScript#Color_and_color_contrast">разделе цвет и цветовой контраст</a>.</p>

<h2 id="Технические_характеристики">Технические характеристики</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Спецификация</th>
   <th scope="col">Статус</th>
   <th scope="col">Пояснения</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('CSS4 Colors', '#colorunits', '&lt;color&gt;')}}</td>
   <td>{{Spec2('CSS4 Colors')}}</td>
   <td>Добавляет <code>rebeccapurple</code>, четырёхзначные (<code>#RGBA</code>) и восьмизначные (<code>#RRGGBBAA</code>) шестнадцатеричные обозначения, <code>rgba() </code>и <code>hsla()</code> в качестве псевдонимов <code>rgb ()</code> и <code>hsl () </code>(оба с одинаковым синтаксисом параметров), разделённые пробелами параметры функции в качестве альтернативы запятым, проценты для Альфа-значений и углы для компонента оттенка в цветах <code>hsl ()</code>.</td>
  </tr>
  <tr>
   <td>{{SpecName('CSS3 Colors', '#colorunits', '&lt;color&gt;')}}</td>
   <td>{{Spec2('CSS3 Colors')}}</td>
   <td>Устаревает системные цвета. Добавляет цвета SVG и функциональные обозначения <code>rgb()</code>, <code>hsl ()</code> и <code>hsla()</code>.</td>
  </tr>
  <tr style="vertical-align: top;">
   <td style="vertical-align: top;">{{SpecName('CSS2.1', 'syndata.html#value-def-color', '&lt;color&gt;')}}</td>
   <td style="vertical-align: top;">{{Spec2('CSS2.1')}}</td>
   <td style="vertical-align: top;">Добавляет <code>orange</code> keyword(ключевое слово) и системные цвета.</td>
  </tr>
  <tr>
   <td style="vertical-align: top;">{{SpecName('CSS1', '#color-units', '&lt;color&gt;')}}</td>
   <td style="vertical-align: top;">{{Spec2('CSS1')}}</td>
   <td style="vertical-align: top;">Первоначальное определение. Включает в себя 16 основных ключевых слов цвета.</td>
  </tr>
 </tbody>
</table>

<h2 id="Совместимость_браузера">Совместимость браузера</h2>
<p>{{Compat}}</p>

<h2 id="Смотреть_также">Смотреть также</h2>

<ul>
 <li>Свойство {{Cssxref("непрозрачность")}} позволяет определить прозрачность на уровне элемента.</li>
 <li>Некоторые общие свойства, которые используют этот тип данных: {{Cssxref("цвет")}}, {{Cssxref("фон")}}, {{Cssxref("бордюр-колор")}}, {{Cssxref("окно-тень")}}, {{Cssxref("контур-цвет")}}, {{Cssxref("текст-тень")}}</li>
 <li><a href="/en-US/docs/Web/HTML/Applying_color">Применение цвета к элементам HTML с помощью CSS</a></li>
</ul>
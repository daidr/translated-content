---
title: Event reference
slug: Web/Events
tags:
  - NeedsTag
  - NeedsTranslation
  - TopicStub
translation_of: Web/Events
---
<p>事件為一些有趣事情，發生後會被傳出以通知code。每個事件被表示為一個根據{{domxref("Event")}}所定義的物件，且可能會有額外自訂欄位與(或)函式來描述發生了什麼事。事件可以表示從使用者互動到自動通知等渲染model所有的事情。</p>

<p>Events are sent to notify code of interesting things that have taken place. Each event is represented by an object which is based on the {{domxref("Event")}} interface, and may have additional custom fields and/or functions used to get additional information about what happened. Events can represent everything from basic user interactions to automated notifications of things happening in the rendering model.</p>

<p>This article offers a list of events that can be sent; some are standard events defined in official specifications, while others are events used internally by specific browsers; for example, Mozilla-specific events are listed so that <a href="/zh-TW/docs/Mozilla/Add-ons">add-ons</a> can use them to interact with the browser.no</p>

<h2 id="標準事件">標準事件</h2>

<p>以下事件是由官方的 Web 標準規範中所定義，且應適用於所有的瀏覽器。下面的清單將列出事件和其所有傳送給事件的物件的 interface （所以你可以看到每個事件需要提供哪些資料）以及事件的定義規範。</p>

<table class="standard-table" style="width: 100%;">
 <tbody>
  <tr>
   <th class="header" style="width: 220px;">事件名稱</th>
   <th class="header" style="width: 90px;">事件類型</th>
   <th class="header" style="width: 100px;">規範</th>
   <th class="header">觸發時機</th>
  </tr>
  <tr>
   <td>{{event("abort")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-abort">DOM L3</a></td>
   <td>The loading of a resource has been aborted.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/abort_(ProgressEvent)">abort</a></code></td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-abort">XMLHttpRequest</a></td>
   <td>Progression has been terminated (not due to an error).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/abort_indexedDB">abort</a></code></td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#database-interface">IndexedDB</a></td>
   <td>A transaction has been aborted.</td>
  </tr>
  <tr>
   <td>{{event("afterprint")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/webappapis.html#printing">HTML5</a></td>
   <td>The associated document has started printing or the print preview has been closed.</td>
  </tr>
  <tr>
   <td>{{event("animationend")}}</td>
   <td>{{domxref("AnimationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>A <a href="/zh-TW/docs/CSS/CSS_animations">CSS animation</a> has completed.</td>
  </tr>
  <tr>
   <td>{{event("animationiteration")}}</td>
   <td>{{domxref("AnimationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>A <a href="/zh-TW/docs/CSS/CSS_animations">CSS animation</a> is repeated.</td>
  </tr>
  <tr>
   <td>{{event("animationstart")}}</td>
   <td>{{domxref("AnimationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>A <a href="/zh-TW/docs/CSS/CSS_animations">CSS animation</a> has started.</td>
  </tr>
  <tr>
   <td>{{event("audioprocess")}}</td>
   <td>{{domxref("AudioProcessingEvent")}}</td>
   <td style="white-space: nowrap;"><a href="https://www.w3.org/TR/webaudio/#AudioProcessingEvent">Web Audio API</a></td>
   <td>The input buffer of a {{domxref("ScriptProcessorNode")}} is ready to be processed.</td>
  </tr>
  <tr>
   <td>{{event("beforeprint")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/webappapis.html#printing">HTML5</a></td>
   <td>The associated document is about to be printed or previewed for printing.</td>
  </tr>
  <tr>
   <td>{{event("beforeunload")}}</td>
   <td>{{domxref("BeforeUnloadEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/browsers.html#unloading-documents">HTML5 </a></td>
   <td></td>
  </tr>
  <tr>
   <td>{{event("beginEvent")}}</td>
   <td>{{domxref("TimeEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-TW/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element begins.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/blocked_indexedDB">blocked</a></code></td>
   <td></td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>An open connection to a database is blocking a <code>versionchange</code> transaction on the same database.</td>
  </tr>
  <tr>
   <td>{{event("blur")}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-blur">DOM L3</a></td>
   <td>An element has lost focus (does not bubble).</td>
  </tr>
  <tr>
   <td>{{event("cached")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The resources listed in the manifest have been downloaded, and the application is now cached.</td>
  </tr>
  <tr>
   <td>{{event("canplay")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-canplay">HTML5 media</a></td>
   <td>The user agent can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.</td>
  </tr>
  <tr>
   <td>{{event("canplaythrough")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-canplaythrough">HTML5 media</a></td>
   <td>The user agent can play the media, and estimates that enough data has been loaded to play the media up to its end without having to stop for further buffering of content.</td>
  </tr>
  <tr>
   <td>{{event("change")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/common-input-element-attributes.html#event-input-change">HTML5</a></td>
   <td>An element loses focus and its value changed since gaining focus.</td>
  </tr>
  <tr>
   <td>{{event("chargingchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The battery begins or stops charging.</td>
  </tr>
  <tr>
   <td>{{event("chargingtimechange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>chargingTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{event("checking")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The user agent is checking for an update, or attempting to download the cache manifest for the first time.</td>
  </tr>
  <tr>
   <td>{{event("click")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-click">DOM L3</a></td>
   <td>A pointing device button has been pressed and released on an element.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/close_websocket">close</a></code></td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been closed.</td>
  </tr>
  <tr>
   <td>{{event("compassneedscalibration")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/orientation-event/#compassneedscalibration">Orientation</a></td>
   <td>The compass used to obtain orientation data is in need of calibration.</td>
  </tr>
  <tr>
   <td>{{event("compositionend")}}</td>
   <td>{{domxref("CompositionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionend">DOM L3</a></td>
   <td>The composition of a passage of text has been completed or canceled.</td>
  </tr>
  <tr>
   <td>{{event("compositionstart")}}</td>
   <td>{{domxref("CompositionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionstart">DOM L3</a></td>
   <td>The composition of a passage of text is prepared (similar to keydown for a keyboard input, but works with other inputs such as speech recognition).</td>
  </tr>
  <tr>
   <td>{{event("compositionupdate")}}</td>
   <td>{{domxref("CompositionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionupdate">DOM L3</a></td>
   <td>A character is added to a passage of text being composed.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/complete_indexedDB">complete</a></code></td>
   <td></td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#transaction">IndexedDB</a></td>
   <td>The transaction successfully completed.</td>
  </tr>
  <tr>
   <td>{{event("contextmenu")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/interactive-elements.html#context-menus">HTML5</a></td>
   <td>The right button of the mouse is clicked (before the context menu is displayed).</td>
  </tr>
  <tr>
   <td>{{event("copy")}}</td>
   <td>{{domxref("ClipboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/clipboard-apis/#copy-event">Clipboard</a></td>
   <td>The text selection has been added to the clipboard.</td>
  </tr>
  <tr>
   <td>{{event("cut")}}</td>
   <td>{{domxref("ClipboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/clipboard-apis/#cut-event">Clipboard</a></td>
   <td>The text selection has been removed from the document and added to the clipboard.</td>
  </tr>
  <tr>
   <td>{{event("dblclick")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-dblclick">DOM L3</a></td>
   <td>A pointing device button is clicked twice on an element.</td>
  </tr>
  <tr>
   <td>{{event("devicehumidity")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dvcs.w3.org/hg/dap/raw-file/tip/sensor-api/Overview.html#datatypes">Sensor</a></td>
   <td>Fresh data is available from a humidity sensor.</td>
  </tr>
  <tr>
   <td>{{event("devicelight")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dvcs.w3.org/hg/dap/raw-file/tip/sensor-api/Overview.html#datatypes">Sensor</a></td>
   <td>Fresh data is available from a light sensor.</td>
  </tr>
  <tr>
   <td>{{event("devicemotion")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/orientation-event/#devicemotion">Orientation</a></td>
   <td>Fresh data is available from a motion sensor.</td>
  </tr>
  <tr>
   <td>{{event("devicenoise")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dvcs.w3.org/hg/dap/raw-file/tip/sensor-api/Overview.html#datatypes">Sensor</a></td>
   <td>Fresh data is available from a noise sensor.</td>
  </tr>
  <tr>
   <td>{{event("deviceorientation")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/orientation-event/#deviceorientation">Orientation</a></td>
   <td>Fresh data is available from an orientation sensor.</td>
  </tr>
  <tr>
   <td>{{event("devicepressure")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dvcs.w3.org/hg/dap/raw-file/tip/sensor-api/Overview.html#datatypes">Sensor</a></td>
   <td>Fresh data is available from a pressure sensor.</td>
  </tr>
  <tr>
   <td>{{event("deviceproximity")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/proximity/Overview.html">Sensor</a></td>
   <td>Fresh data is available from a proximity sensor (indicates an approximated distance between the device and a nearby object).</td>
  </tr>
  <tr>
   <td>{{event("devicetemperature")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dvcs.w3.org/hg/dap/raw-file/tip/sensor-api/Overview.html#datatypes">Sensor</a></td>
   <td>Fresh data is available from a temperature sensor.</td>
  </tr>
  <tr>
   <td>{{event("dischargingtimechange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>dischargingTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td><code>DOMActivate</code> {{deprecated_inline}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMActivate">DOM L3</a></td>
   <td>A button, link or state changing element is activated (use {{event("click")}} instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMAttributeNameChanged</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationNameEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531/#event-type-DOMAttributeNameChanged">DOM L3</a> Removed</td>
   <td>The name of an attribute changed (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMAttrModified</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMAttrModified">DOM L3</a></td>
   <td>The value of an attribute has been modified (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMCharacterDataModified</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMCharacterDataModified">DOM L3</a></td>
   <td>A text or another <a href="/zh-TW/docs/DOM/CharacterData">CharacterData</a> has changed (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td>{{event("DOMContentLoaded")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-end.html#the-end">HTML5</a></td>
   <td>The document has finished loading (but not its dependent resources).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMElementNameChanged</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationNameEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531/#event-type-DOMElementNameChanged">DOM L3</a> Removed</td>
   <td>The name of an element changed (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code>DOMFocusIn</code> {{deprecated_inline}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMFocusIn">DOM L3</a></td>
   <td>An element has received focus (use {{event("focus")}} or {{event("focusin")}} instead).</td>
  </tr>
  <tr>
   <td><code>DOMFocusOut</code> {{deprecated_inline}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMFocusOut">DOM L3</a></td>
   <td>An element has lost focus (use {{event("blur")}} or {{event("focusout")}} instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeInserted</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeInserted">DOM L3</a></td>
   <td>A node has been added as a child of another node (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeInsertedIntoDocument</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeInsertedIntoDocument">DOM L3</a></td>
   <td>A node has been inserted into the document (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeRemoved</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeRemoved">DOM L3</a></td>
   <td>A node has been removed from its parent node (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeRemovedFromDocument</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeRemovedFromDocument">DOM L3</a></td>
   <td>A node has been removed from the document (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMSubtreeModified</a></code> {{deprecated_inline}}</td>
   <td>{{domxref("MutationEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMSubtreeModified">DOM L3</a></td>
   <td>A change happened in the document (use <a href="/zh-TW/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td>{{event("downloading")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The user agent has found an update and is fetching it, or is downloading the resources listed by the cache manifest for the first time.</td>
  </tr>
  <tr>
   <td>{{event("drag")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-drag">HTML5</a></td>
   <td>An element or text selection is being dragged (every 350ms).</td>
  </tr>
  <tr>
   <td>{{event("dragend")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragend">HTML5</a></td>
   <td>A drag operation is being ended (by releasing a mouse button or hitting the escape key).</td>
  </tr>
  <tr>
   <td>{{event("dragenter")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragenter">HTML5</a></td>
   <td>A dragged element or text selection enters a valid drop target.</td>
  </tr>
  <tr>
   <td>{{event("dragleave")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragleave">HTML5</a></td>
   <td>A dragged element or text selection enters a valid drop target.</td>
  </tr>
  <tr>
   <td>{{event("dragover")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragover">HTML5</a></td>
   <td>An element or text selection is being dragged over a valid drop target (every 350ms).</td>
  </tr>
  <tr>
   <td>{{event("dragstart")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragstart">HTML5</a></td>
   <td>The user starts dragging an element or text selection.</td>
  </tr>
  <tr>
   <td>{{event("drop")}}</td>
   <td>{{domxref("DragEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-drop">HTML5</a></td>
   <td>An element is dropped on a valid drop target.</td>
  </tr>
  <tr>
   <td>{{event("durationchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-durationchange">HTML5 media</a></td>
   <td>The <code>duration</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{event("emptied")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-emptied">HTML5 media</a></td>
   <td>The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the <a href="/zh-TW/docs/XPCOM_Interface_Reference/NsIDOMHTMLMediaElement"><code>load()</code></a> method is called to reload it.</td>
  </tr>
  <tr>
   <td>{{event("ended")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-ended">HTML5 media</a></td>
   <td>Playback has stopped because the end of the media was reached.</td>
  </tr>
  <tr>
   <td>{{event("ended_(Web_Audio)", "ended")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://www.w3.org/TR/webaudio/">Web Audio API</a></td>
   <td></td>
  </tr>
  <tr>
   <td>{{event("endEvent")}}</td>
   <td>{{domxref("TimeEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-TW/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element ends.</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-error">DOM L3</a></td>
   <td>A resource failed to load.</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-error">XMLHttpRequest</a></td>
   <td>Progression has failed.</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>An error occurred while downloading the cache manifest or updating the content of the application.</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been closed with prejudice (some data couldn't be sent for example).</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>An event source connection has been failed.</td>
  </tr>
  <tr>
   <td>{{event("error")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>A request caused an error and failed.</td>
  </tr>
  <tr>
   <td>{{event("focus")}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focus">DOM L3</a></td>
   <td>An element has received focus (does not bubble).</td>
  </tr>
  <tr>
   <td>{{event("focusin")}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focusIn">DOM L3</a></td>
   <td>An element is about to receive focus (bubbles).</td>
  </tr>
  <tr>
   <td>{{event("focusout")}}</td>
   <td>{{domxref("FocusEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focusout">DOM L3</a></td>
   <td>An element is about to loose focus (bubbles).</td>
  </tr>
  <tr>
   <td>{{event("fullscreenchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/fullscreen/raw-file/tip/Overview.html#api">Full Screen</a></td>
   <td>An element was turned to fullscreen mode or back to normal mode.</td>
  </tr>
  <tr>
   <td>{{event("fullscreenerror")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/fullscreen/raw-file/tip/Overview.html#api">Full Screen</a></td>
   <td>It was impossible to switch to fullscreen mode for technical reasons or because the permission was denied.</td>
  </tr>
  <tr>
   <td>{{event("gamepadconnected")}}</td>
   <td>{{domxref("GamepadEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/gamepad/#the-gamepadconnected-event">Gamepad</a></td>
   <td>A gamepad has been connected.</td>
  </tr>
  <tr>
   <td>{{event("gamepaddisconnected")}}</td>
   <td>{{domxref("GamepadEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/gamepad/#the-gamepaddisconnected-event">Gamepad</a></td>
   <td>A gamepad has been disconnected.</td>
  </tr>
  <tr>
   <td>{{event("hashchange")}}</td>
   <td>{{domxref("HashChangeEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-hashchange">HTML5</a></td>
   <td>The fragment identifier of the URL has changed (the part of the URL after the #).</td>
  </tr>
  <tr>
   <td>{{event("input")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/forms.html#common-event-behaviors">HTML5</a></td>
   <td>The value of an element changes or the content of an element with the attribute <a href="/zh-TW/docs/DOM/Element.contentEditable">contenteditable</a> is modified.</td>
  </tr>
  <tr>
   <td>{{event("invalid")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#constraint-validation">HTML5</a></td>
   <td>A submittable element has been checked and doesn't satisfy its constraints.</td>
  </tr>
  <tr>
   <td>{{event("keydown")}}</td>
   <td>{{domxref("KeyboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keydown">DOM L3</a></td>
   <td>A key is pressed down.</td>
  </tr>
  <tr>
   <td>{{event("keypress")}}</td>
   <td>{{domxref("KeyboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keypress">DOM L3</a></td>
   <td>A key is pressed down and that key normally produces a character value (use input instead).</td>
  </tr>
  <tr>
   <td>{{event("keyup")}}</td>
   <td>{{domxref("KeyboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keyup">DOM L3</a></td>
   <td>A key is released.</td>
  </tr>
  <tr>
   <td>{{event("levelchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>level</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{event("load")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-load">DOM L3</a></td>
   <td>A resource and its dependent resources have finished loading.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/load_(ProgressEvent)">load</a></code></td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-load">XMLHttpRequest</a></td>
   <td>Progression has been successful.</td>
  </tr>
  <tr>
   <td>{{event("loadeddata")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-loadeddata">HTML5 media</a></td>
   <td>The first frame of the media has finished loading.</td>
  </tr>
  <tr>
   <td>{{event("loadedmetadata")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-loadedmetadata">HTML5 media</a></td>
   <td>The metadata has been loaded.</td>
  </tr>
  <tr>
   <td>{{event("loadend")}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-loadend">XMLHttpRequest</a></td>
   <td>Progress has stopped (after "error", "abort" or "load" have been dispatched).</td>
  </tr>
  <tr>
   <td>{{event("loadstart")}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress </a>and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-loadstart">XMLHttpRequest</a></td>
   <td>Progress has begun.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/message_websocket">message</a></code></td>
   <td>{{domxref("MessageEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A message is received through a WebSocket.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/message_webworker">message</a></code></td>
   <td>{{domxref("MessageEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/workers/#communicating-with-a-dedicated-worker">Web Workers</a></td>
   <td>A message is received from a Web Worker.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/message_webmessaging">message</a></code></td>
   <td>{{domxref("MessageEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/webmessaging/">Web Messaging</a></td>
   <td>A message is received from a child (i)frame or a parent window.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/message_serversentevents">message</a></code></td>
   <td>{{domxref("MessageEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>A message is received through an event source.</td>
  </tr>
  <tr>
   <td>{{event("mousedown")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mousedown">DOM L3</a></td>
   <td>A pointing device button (usually a mouse) is pressed on an element.</td>
  </tr>
  <tr>
   <td>{{event("mouseenter")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseenter">DOM L3</a></td>
   <td>A pointing device is moved onto the element that has the listener attached.</td>
  </tr>
  <tr>
   <td>{{event("mouseleave")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseleave">DOM L3</a></td>
   <td>A pointing device is moved off the element that has the listener attached.</td>
  </tr>
  <tr>
   <td>{{event("mousemove")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mousemove">DOM L3</a></td>
   <td>A pointing device is moved over an element.</td>
  </tr>
  <tr>
   <td>{{event("mouseout")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseout">DOM L3</a></td>
   <td>A pointing device is moved off the element that has the listener attached or off one of its children.</td>
  </tr>
  <tr>
   <td>{{event("mouseover")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseover">DOM L3</a></td>
   <td>A pointing device is moved onto the element that has the listener attached or onto one of its children.</td>
  </tr>
  <tr>
   <td>{{event("mouseup")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseup">DOM L3</a></td>
   <td>A pointing device button is released over an element.</td>
  </tr>
  <tr>
   <td>{{event("noupdate")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The manifest hadn't changed.</td>
  </tr>
  <tr>
   <td>{{event("obsolete")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The manifest was found to have become a 404 or 410 page, so the application cache is being deleted.</td>
  </tr>
  <tr>
   <td>{{event("offline")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html#event-offline">HTML5 offline</a></td>
   <td>The browser has lost access to the network.</td>
  </tr>
  <tr>
   <td>{{event("online")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html#event-online">HTML5 offline</a></td>
   <td>The browser has gained access to the network (but particular websites might be unreachable).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/open_websocket">open</a></code></td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been established.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/open_serversentevents">open</a></code></td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>An event source connection has been established.</td>
  </tr>
  <tr>
   <td>{{event("orientationchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/screen-orientation/">Screen Orientation</a></td>
   <td>The orientation of the device (portrait/landscape) has changed</td>
  </tr>
  <tr>
   <td>{{event("pagehide")}}</td>
   <td>{{domxref("PageTransitionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-pagehide">HTML5</a></td>
   <td>A session history entry is being traversed from.</td>
  </tr>
  <tr>
   <td>{{event("pageshow")}}</td>
   <td>{{domxref("PageTransitionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-pageshow">HTML5</a></td>
   <td>A session history entry is being traversed to.</td>
  </tr>
  <tr>
   <td>{{event("paste")}}</td>
   <td>{{domxref("ClipboardEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/clipboard-apis/#paste-event">Clipboard</a></td>
   <td>Data has been transfered from the system clipboard to the document.</td>
  </tr>
  <tr>
   <td>{{event("pause")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-pause">HTML5 media</a></td>
   <td>Playback has been paused.</td>
  </tr>
  <tr>
   <td>{{event("pointerlockchange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/pointerlock/#pointerlockchange-and-pointerlockerror-events">Pointer Lock</a></td>
   <td>The pointer was locked or released.</td>
  </tr>
  <tr>
   <td>{{event("pointerlockerror")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/pointerlock/#pointerlockchange-and-pointerlockerror-events">Pointer Lock</a></td>
   <td>It was impossible to lock the pointer for technical reasons or because the permission was denied.</td>
  </tr>
  <tr>
   <td>{{event("play")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-play">HTML5 media</a></td>
   <td>Playback has begun.</td>
  </tr>
  <tr>
   <td>{{event("playing")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-playing">HTML5 media</a></td>
   <td>Playback is ready to start after having been paused or delayed due to lack of data.</td>
  </tr>
  <tr>
   <td>{{event("popstate")}}</td>
   <td>{{domxref("PopStateEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-popstate">HTML5</a></td>
   <td>A session history entry is being navigated to (in certain cases).</td>
  </tr>
  <tr>
   <td>{{event("progress")}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-progress">XMLHttpRequest</a></td>
   <td>In progress.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/progress_(appcache_event)">progress</a></code></td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The user agent is downloading resources listed by the manifest.</td>
  </tr>
  <tr>
   <td>{{event("ratechange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-ratechange">HTML5 media</a></td>
   <td>The playback rate has changed.</td>
  </tr>
  <tr>
   <td>{{event("readystatechange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;">HTML5 and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-readystatechange">XMLHttpRequest</a></td>
   <td>The readyState attribute of a document has changed.</td>
  </tr>
  <tr>
   <td>{{event("repeatEvent")}}</td>
   <td>{{domxref("TimeEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-TW/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element is repeated.</td>
  </tr>
  <tr>
   <td>{{event("reset")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#form-submission-0#resetting-a-form">HTML5</a></td>
   <td>A form is reset.</td>
  </tr>
  <tr>
   <td>{{event("resize")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-resize">DOM L3</a></td>
   <td>The document view has been resized.</td>
  </tr>
  <tr>
   <td>{{event("scroll")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-scroll">DOM L3</a></td>
   <td>The document view or an element has been scrolled.</td>
  </tr>
  <tr>
   <td>{{event("seeked")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-seeked">HTML5 media</a></td>
   <td>A <em>seek</em> operation completed.</td>
  </tr>
  <tr>
   <td>{{event("seeking")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-seeking">HTML5 media</a></td>
   <td>A <em>seek</em> operation began.</td>
  </tr>
  <tr>
   <td>{{event("select")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-select">DOM L3</a></td>
   <td>Some text is being selected.</td>
  </tr>
  <tr>
   <td>{{event("show")}}</td>
   <td>{{domxref("MouseEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/html5/interactive-elements.html#context-menus">HTML5</a></td>
   <td>A contextmenu event was fired on/bubbled to an element that has a <a href="/zh-TW/docs/DOM/element.contextmenu">contextmenu</a> attribute</td>
  </tr>
  <tr>
   <td>{{event("stalled")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-stalled">HTML5 media</a></td>
   <td>The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.</td>
  </tr>
  <tr>
   <td>{{event("storage")}}</td>
   <td>{{domxref("StorageEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/webstorage/#the-storage-event">Web Storage</a></td>
   <td>A storage area (<a href="/zh-TW/docs/DOM/Storage#localStorage">localStorage</a> or <a href="/zh-TW/docs/DOM/Storage#sessionStorage">sessionStorage</a>) has changed.</td>
  </tr>
  <tr>
   <td>{{event("submit")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#form-submission-algorithm">HTML5</a></td>
   <td>A form is submitted.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/success_indexedDB">success</a></code></td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>A request successfully completed.</td>
  </tr>
  <tr>
   <td>{{event("suspend")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-suspend">HTML5 media</a></td>
   <td>Media data loading has been suspended.</td>
  </tr>
  <tr>
   <td>{{event("SVGAbort")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>Page loading has been stopped before the <a href="/zh-TW/docs/SVG">SVG</a> was loaded.</td>
  </tr>
  <tr>
   <td>{{event("SVGError")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An error has occurred before the <a href="/zh-TW/docs/SVG">SVG</a> was loaded.</td>
  </tr>
  <tr>
   <td>{{event("SVGLoad")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-TW/docs/SVG">SVG</a> document has been loaded and parsed.</td>
  </tr>
  <tr>
   <td>{{event("SVGResize")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-TW/docs/SVG">SVG</a> document is being resized.</td>
  </tr>
  <tr>
   <td>{{event("SVGScroll")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-TW/docs/SVG">SVG</a> document is being scrolled.</td>
  </tr>
  <tr>
   <td>{{event("SVGUnload")}}</td>
   <td>{{domxref("SVGEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-TW/docs/SVG">SVG</a> document has been removed from a window or frame.</td>
  </tr>
  <tr>
   <td>{{event("SVGZoom")}}</td>
   <td>{{domxref("SVGZoomEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-TW/docs/SVG">SVG</a> document is being zoomed.</td>
  </tr>
  <tr>
   <td>{{event("timeout")}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-timeout">XMLHttpRequest</a></td>
   <td></td>
  </tr>
  <tr>
   <td>{{event("timeupdate")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-timeupdate">HTML5 media</a></td>
   <td>The time indicated by the <code>currentTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{event("touchcancel")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/">Touch Events</a></td>
   <td>A touch point has been disrupted in an implementation-specific manners (too many touch points for example).</td>
  </tr>
  <tr>
   <td>{{event("touchend")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/#the-touchend-event">Touch Events</a></td>
   <td>A touch point is removed from the touch surface.</td>
  </tr>
  <tr>
   <td>{{event("touchenter")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/">Touch Events</a> Removed</td>
   <td>A touch point is moved onto the interactive area of an element.</td>
  </tr>
  <tr>
   <td>{{event("touchleave")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/">Touch Events</a> Removed</td>
   <td>A touch point is moved off the interactive area of an element.</td>
  </tr>
  <tr>
   <td>{{event("touchmove")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/#the-touchmove-event">Touch Events</a></td>
   <td>A touch point is moved along the touch surface.</td>
  </tr>
  <tr>
   <td>{{event("touchstart")}}</td>
   <td>{{domxref("TouchEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/touch-events/#the-touchstart---------event">Touch Events</a></td>
   <td>A touch point is placed on the touch surface.</td>
  </tr>
  <tr>
   <td>{{event("transitionend")}}</td>
   <td>{{domxref("TransitionEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/css3-transitions/#transition-events">CSS Transitions</a></td>
   <td>A <a href="/zh-TW/docs/CSS/CSS_transitions">CSS transition</a> has completed.</td>
  </tr>
  <tr>
   <td>{{event("unload")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-unload">DOM L3</a></td>
   <td>The document or a dependent resource is being unloaded.</td>
  </tr>
  <tr>
   <td>{{event("updateready")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://dev.w3.org/html5/spec/offline.html">Offline</a></td>
   <td>The resources listed in the manifest have been newly redownloaded, and the script can use <code>swapCache()</code> to switch to the new cache.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/upgradeneeded_indexedDB">upgradeneeded</a></code></td>
   <td></td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>An attempt was made to open a database with a version number higher than its current version. A <code>versionchange</code> transaction has been created.</td>
  </tr>
  <tr>
   <td>{{event("userproximity")}}</td>
   <td>{{domxref("SensorEvent")}}</td>
   <td style="white-space: nowrap;"><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/proximity/Overview.html">Sensor</a></td>
   <td>Fresh data is available from a proximity sensor (indicates whether the nearby object is <code>near</code> the device or not).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-TW/docs/Web/Reference/Events/versionchange_indexedDB">versionchange</a></code></td>
   <td></td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/IndexedDB/#database-interface">IndexedDB</a></td>
   <td>A <code>versionchange</code> transaction completed.</td>
  </tr>
  <tr>
   <td>{{event("visibilitychange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/page-visibility/#sec-visibilitychange-event">Page visibility</a></td>
   <td>The content of a tab has become visible or has been hidden.</td>
  </tr>
  <tr>
   <td>{{event("volumechange")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-volumechange">HTML5 media</a></td>
   <td>The volume has changed.</td>
  </tr>
  <tr>
   <td>{{event("waiting")}}</td>
   <td>{{domxref("Event")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-waiting">HTML5 media</a></td>
   <td>Playback has stopped because of a temporary lack of data.</td>
  </tr>
  <tr>
   <td>{{event("wheel")}}</td>
   <td>{{domxref("WheelEvent")}}</td>
   <td style="white-space: nowrap;"><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-wheel">DOM L3</a></td>
   <td>A wheel button of a pointing device is rotated in any direction.</td>
  </tr>
 </tbody>
</table>

<h2 id="非標準事件">非標準事件</h2>

<table class="standard-table" style="width: 100%;">
 <tbody>
  <tr>
   <th class="header" style="width: 220px;">事件名稱</th>
   <th class="header" style="width: 90px;">事件類型</th>
   <th class="header" style="width: 100px;">規範</th>
   <th class="header">觸發時機</th>
  </tr>
  <tr>
   <td>{{event("afterscriptexecute")}}</td>
   <td>{{domxref("Event")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>A script has been executed.</td>
  </tr>
  <tr>
   <td>{{event("beforescriptexecute")}}</td>
   <td>{{domxref("Event")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>A script is about to be executed.</td>
  </tr>
  <tr>
   <td>{{event("cardstatechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{domxref("MozMobileConnection.cardState")}} property changes value.</td>
  </tr>
  <tr>
   <td>{{event("connectionInfoUpdate")}}</td>
   <td></td>
   <td><a href="http://mxr.mozilla.org/mozilla-central/source/dom/wifi/nsIWifi.idl?rev=3e586802f478#176"><em>Firefox OS specific</em></a></td>
   <td>The informations about the signal strength and the link speed have been updated.</td>
  </tr>
  <tr>
   <td>{{event("cfstatechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The call forwarding state changes.</td>
  </tr>
  <tr>
   <td>{{event("datachange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{domxref("MozMobileConnection.data")}} object changes values.</td>
  </tr>
  <tr>
   <td>{{event("dataerror")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{domxref("MozMobileConnection.data")}} object receive an error from the <abbr title="Radio Interface Layer">RIL</abbr>.</td>
  </tr>
  <tr>
   <td>{{event("DOMMouseScroll")}} {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The wheel button of a pointing device is rotated (detail attribute is a number of lines). (use {{event("wheel")}} instead)</td>
  </tr>
  <tr>
   <td><code>dragdrop</code> {{deprecated_inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>An element is dropped (use {{event("drop")}} instead).</td>
  </tr>
  <tr>
   <td><code>dragexit</code> {{deprecated_inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>A drag operation is being ended(use {{event("dragend")}} instead).</td>
  </tr>
  <tr>
   <td><code>draggesture</code> {{deprecated_inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>The user starts dragging an element or text selection (use {{event("dragstart")}} instead).</td>
  </tr>
  <tr>
   <td>{{event("icccardlockerror")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>the {{domxref("MozMobileConnection.unlockCardLock()")}} or {{domxref("MozMobileConnection.setCardLock()")}} methods fails.</td>
  </tr>
  <tr>
   <td>{{event("iccinfochange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{domxref("MozMobileConnection.iccInfo")}} object changes.</td>
  </tr>
  <tr>
   <td>{{event("localized")}}</td>
   <td></td>
   <td><em><a href="https://github.com/fabi1cazenave/webL10n">Mozilla Specific</a></em></td>
   <td>The page has been localized using data-l10n-* attributes.</td>
  </tr>
  <tr>
   <td>{{event("mousewheel")}} {{deprecated_inline}}</td>
   <td></td>
   <td><a href="http://msdn.microsoft.com/zh-TW/library/ie/ms536951%28v=vs.85%29.aspx"><em>IE invented</em></a></td>
   <td>The wheel button of a pointing device is rotated.</td>
  </tr>
  <tr>
   <td>{{event("MozAudioAvailable")}}</td>
   <td>{{domxref("Event")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>The audio buffer is full and the corresponding raw samples are available.</td>
  </tr>
  <tr>
   <td>{{event("MozGamepadAxisMove")}}</td>
   <td></td>
   <td><em>To be specified</em></td>
   <td>A gampad axis is moving.</td>
  </tr>
  <tr>
   <td>{{event("MozGamepadButtonDown")}}</td>
   <td></td>
   <td><em>To be specified</em></td>
   <td>A gamepad button is pressed down.</td>
  </tr>
  <tr>
   <td>{{event("MozGamepadButtonUp")}}</td>
   <td></td>
   <td><em>To be specified</em></td>
   <td>A gamepad button is released.</td>
  </tr>
  <tr>
   <td>{{event("MozMousePixelScroll")}} {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The wheel button of a pointing device is rotated (detail attribute is a number of pixels). (use wheel instead)</td>
  </tr>
  <tr>
   <td>{{event("MozOrientation")}} {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>Fresh data is available from an orientation sensor (see deviceorientation).</td>
  </tr>
  <tr>
   <td>{{event("MozScrolledAreaChanged")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>The document view has been scrolled or resized.</td>
  </tr>
  <tr>
   <td>{{event("moztimechange")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The time of the device has been changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchDown</a> {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is placed on the touch surface (use touchstart instead).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchMove</a> {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is moved along the touch surface (use touchmove instead).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchUp</a> {{deprecated_inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is removed from the touch surface (use touchend instead).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onalerting">onalerting</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The correspondent is being alerted (his/her phone is ringing).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onbusy">onbusy</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The line of the correspondent is busy.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/oncallschanged">oncallschanged</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been added or removed from the list of current calls.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onconnected">onconnected</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been connected.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onconnecting">onconnecting</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to connect.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/ondelivered">ondelivered</a></td>
   <td>{{domxref("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been successfully delivered.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/ondialing">ondialing</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The number of a correspondent has been dialed.</td>
  </tr>
  <tr>
   <td>{{event("ondisabled")}}</td>
   <td></td>
   <td><a href="http://mxr.mozilla.org/mozilla-central/source/dom/wifi/nsIWifi.idl?rev=3e586802f478#182"><em>Firefox OS specific</em></a></td>
   <td>Wifi has been disabled on the device.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/ondisconnected">ondisconnected</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been disconnected.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/ondisconnecting">ondisconnecting</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to disconnect.</td>
  </tr>
  <tr>
   <td>{{event("onenabled")}}</td>
   <td></td>
   <td><a href="http://mxr.mozilla.org/mozilla-central/source/dom/wifi/nsIWifi.idl?rev=3e586802f478#182"><em>Firefox OS specific</em></a></td>
   <td>Wifi has been enabled on the device.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onerror_call_event">onerror</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An error occurred.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onheld">onheld</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been held.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onholding">onholding</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to be held.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onincoming">onincoming</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is being received.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onreceived">onreceived</a></td>
   <td>{{domxref("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been received.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onresuming">onresuming</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to resume.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onsent">onsent</a></td>
   <td>{{domxref("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been sent.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/DOM/onstatechange">onstatechange</a></td>
   <td>{{domxref("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The state of a call has changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/onstatusChange">onstatuschange</a></td>
   <td></td>
   <td><a href="http://mxr.mozilla.org/mozilla-central/source/dom/wifi/nsIWifi.idl?rev=3e586802f478#156"><em>Firefox OS specific</em></a></td>
   <td>The status of the Wifi connection changed.</td>
  </tr>
  <tr>
   <td>{{event("overflow")}}</td>
   <td>{{domxref("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>An element has been overflowed by its content or has been rendered for the first time in this state (only works for elements styled with <code>overflow</code> != <code>visible</code>).</td>
  </tr>
  <tr>
   <td>{{event("smartcard-insert")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A <a href="/zh-TW/docs/JavaScript_crypto">smartcard</a> has been inserted.</td>
  </tr>
  <tr>
   <td>{{event("smartcard-remove")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A <a href="/zh-TW/docs/JavaScript_crypto">smartcard</a> has been removed.</td>
  </tr>
  <tr>
   <td>{{event("stkcommand")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The <abbr title="SIM Application Toolkit">STK</abbr> Proactive Command is issued from <abbr title="Integrated Circuit Card">ICC</abbr>.</td>
  </tr>
  <tr>
   <td>{{event("stksessionend")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The <abbr title="SIM Application Toolkit">STK</abbr> Session is terminated by <abbr title="Integrated Circuit Card">ICC</abbr>.</td>
  </tr>
  <tr>
   <td><code>text</code></td>
   <td></td>
   <td><em>Mozilla Specific</em></td>
   <td>A generic composition event occurred.</td>
  </tr>
  <tr>
   <td>{{event("underflow")}}"</td>
   <td>{{domxref("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>An element is no longer overflowed by its content (only works for elements styled with <code>overflow</code> != <code>visible</code>).</td>
  </tr>
  <tr>
   <td><code>uploadprogress</code> {{deprecated_inline}}</td>
   <td>{{domxref("ProgressEvent")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>Upload is in progress (see {{event("progress")}}).</td>
  </tr>
  <tr>
   <td>{{event("ussdreceived")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>A new <abbr title="Unstructured Supplementary Service Data">USSD</abbr> message is received</td>
  </tr>
  <tr>
   <td>{{event("voicechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{domxref("MozMobileConnection.voice")}} object changes values.</td>
  </tr>
 </tbody>
</table>

<h2 id="Mozilla_專屬事件">Mozilla 專屬事件</h2>

<div class="note">
<p><strong>Note:</strong> 以下事件從未在網頁上觸發。它們僅在能在 chrome content context 上使用。</p>
</div>

<h3 id="XUL_事件">XUL 事件</h3>

<table class="standard-table" style="width: 100%;">
 <tbody>
  <tr>
   <th class="header" style="width: 220px;">事件名稱</th>
   <th class="header" style="width: 90px;">事件類型</th>
   <th class="header" style="width: 100px;">規範</th>
   <th class="header">觸發時機</th>
  </tr>
  <tr>
   <td>{{event("broadcast")}}</td>
   <td></td>
   <td><a href="/zh-TW/docs/XUL/Tutorial/Broadcasters_and_Observers#Broadcast_event">XUL</a></td>
   <td>An <code>observer</code> noticed a change to the attributes of a watched broadcaster.</td>
  </tr>
  <tr>
   <td>{{event("CheckboxStateChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The state of a <code>checkbox</code> has been changed either by a user action or by a script (useful for accessibility).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/close_event">close</a></td>
   <td></td>
   <td>XUL</td>
   <td>The close button of the window has been clicked.</td>
  </tr>
  <tr>
   <td>{{event("command")}}</td>
   <td></td>
   <td>XUL</td>
   <td>An element has been activated.</td>
  </tr>
  <tr>
   <td>{{event("commandupdate")}}</td>
   <td></td>
   <td>XUL</td>
   <td>A command update occurred on a <code>commandset</code> element.</td>
  </tr>
  <tr>
   <td>{{event("DOMMenuItemActive")}}</td>
   <td></td>
   <td>XUL</td>
   <td>A menu or menuitem has been hovered or highlighted.</td>
  </tr>
  <tr>
   <td>{{event("DOMMenuItemInactive")}}</td>
   <td></td>
   <td><em>XUL</em></td>
   <td>A menu or menuitem is no longer hovered or highlighted.</td>
  </tr>
  <tr>
   <td>{{event("popuphidden")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-TW/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip has been hidden.</td>
  </tr>
  <tr>
   <td>{{event("popuphiding")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-TW/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip is about to be hidden.</td>
  </tr>
  <tr>
   <td>{{event("popupshowing")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-TW/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip is about to become visible.</td>
  </tr>
  <tr>
   <td>{{event("popupshown")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-TW/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip has become visible.</td>
  </tr>
  <tr>
   <td>{{event("RadioStateChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The state of a <code>radio</code> has been changed either by a user action or by a script (useful for accessibility).</td>
  </tr>
  <tr>
   <td>{{event("ValueChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The value of an element has changed (a progress bar for example, useful for accessibility).</td>
  </tr>
 </tbody>
</table>

<h3 id="附加元件專屬事件">附加元件專屬事件</h3>

<table class="standard-table" style="width: 100%;">
 <tbody>
  <tr>
   <th class="header" style="width: 220px;">事件名稱</th>
   <th class="header" style="width: 90px;">事件類型</th>
   <th class="header" style="width: 100px;">規範</th>
   <th class="header">觸發時機</th>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozSwipeGesture">MozSwipeGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A touch point is swiped across the touch surface</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGestureStart">MozMagnifyGestureStart</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points start to move away from each other.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGestureUpdate">MozMagnifyGestureUpdate</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points move away from each other (after a MozMagnifyGestureStart).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGesture">MozMagnifyGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points moved away from each other (after a sequence of MozMagnifyGestureUpdate).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozRotateGestureStart">MozRotateGestureStart</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points start to rotate around a point.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozRotateGestureUpdate">MozRotateGestureUpdate</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points rotate around a point (after a MozRotateGestureStart).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozRotateGesture">MozRotateGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points rotate around a point (after a sequence of MozRotateGestureUpdate).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozTapGesture">MozTapGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points are tapped on the touch surface.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozPressTapGesture">MozPressTapGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A "press-tap" gesture happened on the touch surface (first finger down, second finger down, second finger up, first finger up).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozEdgeUIGesture">MozEdgeUIGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A touch point is swiped across the touch surface to invoke the edge UI (Win8 only).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozAfterPaint">MozAfterPaint</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Content has been repainted.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozBeforeResize">MozBeforeResize</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window is about to be resized.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMPopupBlocked">DOMPopupBlocked</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A popup has been blocked</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMWindowCreated">DOMWindowCreated</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window has been created.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMWindowClose">DOMWindowClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window is about to be closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMTitleChanged">DOMTitleChanged</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>The title of a window has changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMLinkAdded">DOMLinkAdded</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>A link has been added a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMLinkRemoved">DOMLinkRemoved</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>A link has been removed inside from a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMMetaAdded">DOMMetaAdded</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code>meta</code> element has been added to a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMMetaRemoved">DOMMetaRemoved</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code>meta</code> element has been removed from a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMWillOpenModalDialog">DOMWillOpenModalDialog</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A modal dialog is about to open.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMModalDialogClosed">DOMModalDialogClosed</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A modal dialog has been closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMAutoComplete">DOMAutoComplete</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The content of an element has been auto-completed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/DOMFrameContentLoaded">DOMFrameContentLoaded</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The frame has finished loading (but not its dependent resources).</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/AlertActive">AlertActive</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code><a href="/zh-TW/docs/XUL/notification">notification</a></code> element is shown.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/AlertClose">AlertClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code><a href="/zh-TW/docs/XUL/notification">notification</a></code> element is closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/fullscreen">fullscreen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Browser fullscreen mode has been entered or left.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/sizemodechange">sizemodechange</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Window has entered/left fullscreen mode, or has been minimized/unminimized.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/MozEnteredDomFullscreen">MozEnteredDomFullscreen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td><a href="/zh-TW/docs/DOM/Using_full-screen_mode">DOM fullscreen</a> mode has been entered.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSWindowClosing">SSWindowClosing</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The session store will stop tracking this window.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSTabClosing">SSTabClosing</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The session store will stop tracking this tab.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSTabRestoring">SSTabRestoring</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab is about to be restored.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSTabRestored">SSTabRestored</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been restored.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSWindowStateReady">SSWindowStateReady</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window state has switched to "ready".</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/SSWindowStateBusy">SSWindowStateBusy</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window state has switched to "busy".</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/tabviewsearchenabled">tabviewsearchenabled</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The search feature of Panorama has been activated</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/tabviewsearchdisabled">tabviewsearchdisabled</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The search feature of Panorama has been deactivated</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/tabviewframeinitialized">tabviewframeinitialized</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The frame container of Panorama has been initialized</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/tabviewshown">tabviewshown</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The Panorama tab has been shown</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/tabviewhidden">tabviewhidden</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The Panorama tab has been hidden</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabOpen">TabOpen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been opened.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabClose">TabClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabSelect">TabSelect</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been selected.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabShow">TabShow</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been shown.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabHide">TabHide</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been hidden.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabPinned">TabPinned</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been pinned.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/TabUnpinned">TabUnpinned</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been unpinned.</td>
  </tr>
 </tbody>
</table>

<h3 id="開發者工具（Developer_tool_）專屬事件">開發者工具（Developer tool ）專屬事件</h3>

<table class="standard-table" style="width: 100%;">
 <tbody>
  <tr>
   <th class="header" style="width: 220px;">事件名稱</th>
   <th class="header" style="width: 90px;">事件類型</th>
   <th class="header" style="width: 100px;">規範</th>
   <th class="header">觸發時機</th>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewRefreshed">CssRuleViewRefreshed</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>The "Rules" view of the style inspector has been updated.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewChanged">CssRuleViewChanged</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>The "Rules" view of the style inspector has been changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewCSSLinkClicked">CssRuleViewCSSLinkClicked</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>A link to a CSS file has been clicked in the "Rules" view of the style inspector.</td>
  </tr>
 </tbody>
</table>

<h2 id="事件分類">事件分類</h2>

<h3 id="動畫事件（Animation_events）">動畫事件（Animation events）</h3>

<p>{{event("animationend")}}, {{event("animationiteration")}}, {{event("animationstart")}}, {{event("beginEvent")}}, {{event("endEvent")}}, {{event("repeatEvent")}}</p>

<h3 id="電池相關事件（Battery_events）">電池相關事件（Battery events）</h3>

<p>{{event("chargingchange")}} {{event("chargingtimechange")}}, {{event("dischargingtimechange")}} {{event("levelchange")}}</p>

<h3 id="電話事件（Call_events）">電話事件（Call events）</h3>

<p>{{event("alerting")}}, {{event("busy")}}, {{event("callschanged")}} {{event("cfstatechange")}}, {{event("connected")}}, {{event("connecting")}}, {{event("dialing")}}, {{event("disconnected")}}, {{event("disconnecting")}}, {{event("error_(Telephony)","error")}}, {{event("held")}}, {{event("holding")}}, {{event("incoming")}}, {{event("resuming")}}, {{event("statechange")}}, {{event("voicechange")}}</p>

<h3 id="CSS_事件">CSS 事件</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewRefreshed">CssRuleViewRefreshed</a>, <a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewChanged">CssRuleViewChanged</a>, <a href="/zh-TW/docs/Web/Reference/Events/CssRuleViewCSSLinkClicked">CssRuleViewCSSLinkClicked</a>, {{event("transitionend")}}</p>

<h3 id="資料庫事件">資料庫事件</h3>

<p><code><a href="/zh-TW/docs/Web/Reference/Events/abort_indexedDB">abort</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/blocked_indexedDB">blocked</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/complete_indexedDB">complete</a></code>, {{event("error")}} (<a href="/zh-TW/docs/Web/Reference/Events/error">link</a>), <code><a href="/zh-TW/docs/Web/Reference/Events/success_indexedDB">success</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/upgradeneeded_indexedDB">upgradeneeded</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/versionchange_indexedDB">versionchange</a></code></p>

<h3 id="Document_事件">Document 事件</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/DOMLinkAdded">DOMLinkAdded</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMLinkRemoved">DOMLinkRemoved</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMMetaAdded">DOMMetaAdded</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMMetaRemoved">DOMMetaRemoved</a>,<a href="/zh-TW/docs/Web/Reference/Events/DOMWillOpenModalDialog">DOMWillOpenModalDialog</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMModalDialogClosed">DOMModalDialogClosed</a>, {{event("unload")}}</p>

<h3 id="DOM_mutation_events">DOM mutation events</h3>

<p><code><a href="/zh-TW/docs/DOM/Mutation_events">DOMAttributeNameChanged</a></code>, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMAttrModified</a></code>, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMCharacterDataModified</a></code>, {{event("DOMContentLoaded")}}, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMElementNameChanged</a></code>, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeInserted</a></code>,<code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeInsertedIntoDocument</a></code>, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeRemoved</a></code>, <code><a href="/zh-TW/docs/DOM/Mutation_events">DOMNodeRemovedFromDocument</a></code>,<code><a href="/zh-TW/docs/DOM/Mutation_events">DOMSubtreeModified</a></code></p>

<h3 id="拖曳事件">拖曳事件</h3>

<p>{{event("drag")}}, <code>dragdrop</code>, {{event("dragend")}}, {{event("dragenter")}}, <code>dragexit</code>, <code>draggesture</code>, {{event("dragleave")}}, {{event("dragover")}}, {{event("dragstart")}}, {{event("drop")}}</p>

<h3 id="元素相關事件">元素相關事件</h3>

<p>{{event("invalid")}}, {{event("overflow")}}, {{event("underflow")}}, <a href="/zh-TW/docs/Web/Reference/Events/DOMAutoComplete">DOMAutoComplete</a>, {{event("command")}}, {{event("commandupdate")}}</p>

<h3 id="Focus_events">Focus events</h3>

<p>{{event("blur")}}, {{event("change")}}, <code>DOMFocusIn</code>, <code>DOMFocusOut</code>, {{event("focus")}}, {{event("focusin")}}, {{event("focusout")}}</p>

<h3 id="表單相關事件">表單相關事件</h3>

<p>{{event("reset")}}, {{event("submit")}}</p>

<h3 id="Frame_相關事件">Frame 相關事件</h3>

<p>{{event("mozbrowserclose")}}, {{event("mozbrowsercontextmenu")}}, {{event("mozbrowsererror")}}, {{event("mozbrowsericonchange")}}, {{event("mozbrowserlocationchange")}}, {{event("mozbrowserloadend")}}, {{event("mozbrowserloadstart")}}, {{event("mozbrowseropenwindow")}}, {{event("mozbrowsersecuritychange")}}, {{event("mozbrowsershowmodalprompt")}} (<a href="/zh-TW/docs/Web/Reference/Events/mozbrowsershowmodalprompt">link</a>), {{event("mozbrowsertitlechange")}}, <a href="/zh-TW/docs/Web/Reference/Events/DOMFrameContentLoaded">DOMFrameContentLoaded</a></p>

<h3 id="Input_device_events">Input device events</h3>

<p>{{event("click")}}, {{event("contextmenu")}}, {{event("DOMMouseScroll")}}, {{event("dblclick")}}, {{event("gamepadconnected")}}, {{event("gamepaddisconnected")}}, {{event("keydown")}}, {{event("keypress")}}, {{event("keyup")}}, {{event("MozGamepadButtonDown")}}, {{event("MozGamepadButtonUp")}}, {{event("mousedown")}}, {{event("mouseenter")}}, {{event("mouseleave")}}, {{event("mousemove")}}, {{event("mouseout")}}, {{event("mouseover")}}, {{event("mouseup")}}, {{event("mousewheel")}}, {{event("MozMousePixelScroll")}}, {{event("pointerlockchange")}}, {{event("pointerlockerror")}},{{event("wheel")}}</p>

<h3 id="多媒體事件">多媒體事件</h3>

<p>{{event("audioprocess")}}, {{event("canplay")}}, {{event("canplaythrough")}}, {{event("durationchange")}}, {{event("emptied")}}, {{event("ended")}}, {{event("ended_(Web_Audio)", "ended")}}, {{event("loadeddata")}}, {{event("loadedmetadata")}}, {{event("MozAudioAvailable")}}, {{event("pause")}}, {{event("play")}}, {{event("playing")}}, {{event("ratechange")}}, {{event("seeked")}}, {{event("seeking")}}, {{event("stalled")}}, {{event("suspend")}}, {{event("timeupdate")}}, {{event("volumechange")}}, {{event("waiting")}}, {{event("complete")}}</p>

<h3 id="目錄事件">目錄事件</h3>

<p>{{event("DOMMenuItemActive")}}, {{event("DOMMenuItemInactive")}}</p>

<h3 id="網路相關事件">網路相關事件</h3>

<p>{{event("datachange")}}, {{event("dataerror")}}, {{event("disabled")}}, {{event("enabled")}}, {{event("offline")}}, {{event("online")}}, {{event("statuschange")}}, {{event("connectionInfoUpdate")}},</p>

<h3 id="Notification_events">Notification events</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/AlertActive">AlertActive</a>, <a href="/zh-TW/docs/Web/Reference/Events/AlertClose">AlertClose</a></p>

<h3 id="Pointer_events">Pointer events</h3>

<p>{{event("pointerover")}}, {{event("pointerenter")}}, {{event("pointerdown")}}, {{event("pointermove")}}, {{event("pointerup")}}, {{event("pointercancel")}}, {{event("pointerout")}}, {{event("pointerleave")}}, {{event("gotpointercapture")}}, {{event("lostpointercapture")}}</p>

<h3 id="Popup_events">Popup events</h3>

<p>{{event("popuphidden")}}, {{event("popuphiding")}}, {{event("popupshowing")}}, {{event("popupshown")}}, <a href="/zh-TW/docs/Web/Reference/Events/DOMPopupBlocked">DOMPopupBlocked</a></p>

<h3 id="列印相關事件">列印相關事件</h3>

<p>{{event("afterprint")}}, {{event("beforeprint")}}</p>

<h3 id="Progress_events">Progress events</h3>

<p><code><a href="/zh-TW/docs/Web/Reference/Events/abort_(ProgressEvent)">abort</a></code>, {{event("error")}}, <code><a href="/zh-TW/docs/Web/Reference/Events/load_(ProgressEvent)">load</a></code>, {{event("loadend")}}, {{event("loadstart")}}, {{event("progress")}},<code><a href="/zh-TW/docs/Web/Reference/Events/progress_(appcache_event)">progress</a></code>, {{event("timeout")}}, <code>uploadprogress</code></p>

<h3 id="Resource_events">Resource events</h3>

<p>{{event("abort")}}, {{event("cached")}}, {{event("error")}}, {{event("load")}}</p>

<h3 id="Script_events">Script events</h3>

<p>{{event("afterscriptexecute")}}, {{event("beforescriptexecute")}}</p>

<h3 id="Sensor_events">Sensor events</h3>

<p>{{event("compassneedscalibration")}}, {{event("devicelight")}}, {{event("devicemotion")}}, {{event("deviceorientation")}}, {{event("deviceproximity")}}, {{event("MozOrientation")}}, {{event("orientationchange")}}, {{event("userproximity")}}</p>

<h3 id="Session_history_events">Session history events</h3>

<p>{{event("pagehide")}}, {{event("pageshow")}}, {{event("popstate")}}</p>

<h3 id="Smartcard_events">Smartcard events</h3>

<p>{{event("icccardlockerror")}}, {{event("iccinfochange")}}, {{event("smartcard-insert")}}, {{event("smartcard-remove")}}, {{event("stkcommand")}}, {{event("stksessionend")}}, {{event("cardstatechange")}}</p>

<h3 id="SMS_and_USSD_events">SMS and USSD events</h3>

<p>{{event("delivered")}}, {{event("received")}}, {{event("sent")}}, {{event("ussdreceived")}}</p>

<h3 id="Storage_events">Storage events</h3>

<p>{{event("change")}} (see <a href="#非標準事件">Non-standard events</a>), {{event("storage")}}</p>

<h3 id="SVG_事件">SVG 事件</h3>

<p>{{event("SVGAbort")}}, {{event("SVGError")}}, {{event("SVGLoad")}}, {{event("SVGResize")}}, {{event("SVGScroll")}}, {{event("SVGUnload")}}, {{event("SVGZoom")}}</p>

<h3 id="Tab_events">Tab events</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/tabviewsearchenabled">tabviewsearchenabled</a>, <a href="/zh-TW/docs/Web/Reference/Events/tabviewsearchdisabled">tabviewsearchdisabled</a>, <a href="/zh-TW/docs/Web/Reference/Events/tabviewframeinitialized">tabviewframeinitialized</a>, <a href="/zh-TW/docs/Web/Reference/Events/tabviewshown">tabviewshown</a>,<a href="/zh-TW/docs/Web/Reference/Events/tabviewhidden">tabviewhidden</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabOpen">TabOpen</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabClose">TabClose</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabSelect">TabSelect</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabShow">TabShow</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabHide">TabHide</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabPinned">TabPinned</a>, <a href="/zh-TW/docs/Web/Reference/Events/TabUnpinned">TabUnpinned</a>,<a href="/zh-TW/docs/Web/Reference/Events/SSTabClosing">SSTabClosing</a>, <a href="/zh-TW/docs/Web/Reference/Events/SSTabRestoring">SSTabRestoring</a>, <a href="/zh-TW/docs/Web/Reference/Events/SSTabRestored">SSTabRestored</a>, {{event("visibilitychange")}}</p>

<h3 id="Text_events">Text events</h3>

<p>{{event("compositionend")}}, {{event("compositionstart")}}, {{event("compositionupdate")}}, {{event("copy")}}, {{event("cut")}}, {{event("paste")}}, {{event("select")}}, <code>text</code></p>

<h3 id="Touch_events">Touch events</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/MozEdgeUIGesture">MozEdgeUIGesture</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGesture">MozMagnifyGesture</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGestureStart">MozMagnifyGestureStart</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozMagnifyGestureUpdate">MozMagnifyGestureUpdate</a>,<a href="/zh-TW/docs/Web/Reference/Events/MozPressTapGesture">MozPressTapGesture</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozRotateGesture">MozRotateGesture</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozRotateGestureStart">MozRotateGestureStart</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozRotateGestureUpdate">MozRotateGestureUpdate</a>,<a href="/zh-TW/docs/Web/Reference/Events/MozSwipeGesture">MozSwipeGesture</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozTapGesture">MozTapGesture</a>, <a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchDown</a>, <a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchMove</a>, <a href="/zh-TW/DOM/Touch_events_(Mozilla_experimental)">MozTouchUp</a>, {{event("touchcancel")}}, {{event("touchend")}}, {{event("touchenter")}}, {{event("touchleave")}}, {{event("touchmove")}}, {{event("touchstart")}}</p>

<h3 id="Update_events">Update events</h3>

<p>{{event("checking")}}, {{event("downloading")}}, {{event("error")}}, {{event("noupdate")}}, {{event("obsolete")}}, {{event("updateready")}}</p>

<h3 id="Value_change_events">Value change events</h3>

<p>{{event("broadcast")}}, {{event("CheckboxStateChange")}}, {{event("hashchange")}}, {{event("input")}}, {{event("RadioStateChange")}}, {{event("readystatechange")}}, {{event("ValueChange")}}</p>

<h3 id="View_events">View events</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/fullscreen">fullscreen</a>, {{event("fullscreenchange")}}, {{event("fullscreenerror")}}, <a href="/zh-TW/docs/Web/Reference/Events/MozEnteredDomFullscreen">MozEnteredDomFullscreen</a>, {{event("MozScrolledAreaChanged")}}, {{event("resize")}}, {{event("scroll")}}, <a href="/zh-TW/docs/Web/Reference/Events/sizemodechange">sizemodechange</a></p>

<h3 id="Websocket_事件">Websocket 事件</h3>

<p><code><a href="/zh-TW/docs/Web/Reference/Events/close_websocket">close</a></code>, {{event("error")}}, <code><a href="/zh-TW/docs/Web/Reference/Events/message_websocket">message</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/open_websocket">open</a></code></p>

<h3 id="Window_events">Window events</h3>

<p><a href="/zh-TW/docs/Web/Reference/Events/DOMWindowCreated">DOMWindowCreated</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMWindowClose">DOMWindowClose</a>, <a href="/zh-TW/docs/Web/Reference/Events/DOMTitleChanged">DOMTitleChanged</a>, <a href="/zh-TW/docs/Web/Reference/Events/MozBeforeResize">MozBeforeResize</a> {{Deprecated_Inline}},<a href="/zh-TW/docs/Web/Reference/Events/SSWindowClosing">SSWindowClosing</a>, <a href="/zh-TW/docs/Web/Reference/Events/SSWindowStateReady">SSWindowStateReady</a>, <a href="/zh-TW/docs/Web/Reference/Events/SSWindowStateBusy">SSWindowStateBusy</a>, <a href="/zh-TW/docs/Web/Reference/Events/close_event">close</a></p>

<h3 id="尚未分類的事件">尚未分類的事件</h3>

<p>{{event("beforeunload")}}, {{event("localized")}}, <code><a href="/zh-TW/docs/Web/Reference/Events/message_webworker">message</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/message_webmessaging">message</a></code>, <code><a href="/zh-TW/docs/Web/Reference/Events/message_serversentevents">message</a></code>, <a href="/zh-TW/docs/Web/Reference/Events/MozAfterPaint">MozAfterPaint</a>, {{event("moztimechange")}}, <code><a href="/zh-TW/docs/Web/Reference/Events/open_serversentevents">open</a></code>, {{event("show")}}</p>

<h2 id="規範">規範</h2>

{{Specifications}}

<h2 id="參見">參見</h2>

<ul>
 <li>{{domxref("Event")}}</li>
 <li><a href="/zh-TW/docs/Web/Guide/DOM/Events">Event developer guide</a></li>
</ul>
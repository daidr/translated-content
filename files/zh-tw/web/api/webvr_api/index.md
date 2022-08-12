---
title: WebVR API
slug: Web/API/WebVR_API
translation_of: Web/API/WebVR_API
---
<div>{{SeeCompatTable}}{{APIRef("WebVR API")}}</div>

<p>WebVR 可以讓穿戴的VR裝置 (如頭戴裝置 Oculus Rift 或 HTC Vive) 與 web 應用程式結合。開發人員可以將VR裝置所提供的位置與動作資訊轉移到3D的場景中。利用 WebVR可以創造出很多有趣的應用程式: 包含虛擬導覽、互動訓練軟體等等。</p>

<h2 id="用法與基本觀念">用法與基本觀念</h2>

<p>透過呼叫 {{domxref("Navigator.getVRDisplays()")}} 函數可以得到與電腦連接的VR裝置，每個裝置會回傳一個 {{domxref("VRDisplay")}} 物件</p>

<p><img alt='Sketch of a person in a chair with wearing goggles labelled "Head mounted display (HMD)" facing a monitor with a webcam labelled "Position sensor"' src="hw-setup.png"></p>

<p>{{domxref("VRDisplay")}} 是 WebVR API 的核心，提供以下功能:</p>

<ul>
 <li>Retrieve useful information to allow us to identify the display, what capabilities it has, controllers associated with it, and more.</li>
 <li>Retrieve {{domxref("VRFrameData", "frame data")}} for each frame of content you you want to present in a display, and submit those frames for display at a consistent rate.</li>
 <li>Start and stop presenting to the display.</li>
</ul>

<p>A typical (simple) WebVR app would work like so:</p>

<ol>
 <li>呼叫 {{domxref("Navigator.getVRDisplays()")}} 來取得 VR 顯示器的 reference。</li>
 <li>呼叫 {{domxref("VRDisplay.requestPresent()")}} 來啟動 VR顯示器。</li>
 <li>WebVR's dedicated {{domxref("VRDisplay.requestAnimationFrame()")}} method is used to run the app's rendering loop at the correct refresh rate for the display.</li>
 <li>Inside the rendering loop, you grab the data required to display the current frame ({{domxref("VRDisplay.getFrameData()")}}), draw the displayed scene twice — once for the view in each eye, then submit the rendered view to the display to show to the user ({{domxref("VRDisplay.submitFrame()")}}).</li>
</ol>

<p>In addition, WebVR 1.1 adds a number of events on the {{domxref("Window")}} object to allow JavaScript to respond to changes to the status of the display.</p>

<div class="note">
<p><strong>Note</strong>: You can find a lot more out about how the API works in our <a href="/en-US/docs/Web/API/WebVR_API/Using_the_WebVR_API">Using the WebVR API</a> and <a href="/en-US/docs/Web/API/WebVR_API/Concepts">WebVR Concepts</a> articles.</p>
</div>

<h3 id="Using_controllers_Combining_WebVR_with_the_Gamepad_API">Using controllers: Combining WebVR with the Gamepad API</h3>

<p>Many WebVR hardware setups feature controllers that go along with the headset. These can be used in WebVR apps via the <a href="/en-US/docs/Web/API/Gamepad_API">Gamepad API</a>, and specifically the <a href="/en-US/docs/Web/API/Gamepad_API#Experimental_Gamepad_extensions">Gamepad Extensions API</a> that adds API features for accessing <a href="/en-US/docs/Web/API/GamepadPose">controller pose</a>, <a href="/en-US/docs/Web/API/GamepadHapticActuator">haptic actuators</a>, and more.</p>

<div class="note">
<p><strong>Note</strong>: Our <a href="/en-US/docs/Web/API/WebVR_API/Using_VR_controllers_with_WebVR">Using VR controllers with WebVR</a> article explains the basics of how to use VR controllers with WebVR apps.</p>
</div>

<h2 id="WebVR_Interfaces">WebVR Interfaces</h2>

<dl>
 <dt>{{domxref("VRDisplay")}}</dt>
 <dd>Represents any VR device supported by this API. It includes generic information such as device IDs and descriptions, as well as methods for starting to present a VR scene, retrieving eye parameters and display capabilities, and other important functionality.</dd>
 <dt>{{domxref("VRDisplayCapabilities")}}</dt>
 <dd>Describes the capabilities of a {{domxref("VRDisplay")}} — it's features can be used to perform VR device capability tests, for example can it return position information.</dd>
 <dt>{{domxref("VRDisplayEvent")}}</dt>
 <dd>Represents the event object of WebVR-related events (see the <a href="#window">window object extensions</a> listed below).</dd>
 <dt>{{domxref("VRFrameData")}}</dt>
 <dd>Represents all the information needed to render a single frame of a VR scene; constructed by {{domxref("VRDisplay.getFrameData()")}}.</dd>
 <dt>{{domxref("VRPose")}}</dt>
 <dd>Represents the position state at a given timestamp (which includes orientation, position, velocity, and acceleration.)</dd>
 <dt>{{domxref("VREyeParameters")}}</dt>
 <dd>Provides access to all the information required to correctly render a scene for each given eye, including field of view information.</dd>
 <dt>{{domxref("VRFieldOfView")}}</dt>
 <dd>Represents a field of view defined by 4 different degree values describing the view from a center point.</dd>
 <dt>{{domxref("VRLayerInit")}}</dt>
 <dd>Represents a layer to be presented in a {{domxref("VRDisplay")}}.</dd>
 <dt>{{domxref("VRStageParameters")}}</dt>
 <dd>Represents the values describing the the stage area for devices that support room-scale experiences.</dd>
</dl>

<h3 id="Extensions_to_other_interfaces">Extensions to other interfaces</h3>

<p>The WebVR API extends the following APIs, adding the listed features.</p>

<h4 id="Gamepad">Gamepad</h4>

<dl>
 <dt>{{domxref("Gamepad.displayId")}} {{readonlyInline}}</dt>
 <dd><dfn>Returns the {{domxref("VRDisplay.displayId")}} of the associated {{domxref("VRDisplay")}} — the <code>VRDisplay</code> that the gamepad is controlling the displayed scene of.</dfn></dd>
</dl>

<h4 id="Navigator">Navigator</h4>

<dl>
 <dt>{{domxref("Navigator.activeVRDisplays")}} {{readonlyInline}}</dt>
 <dd>Returns an array containing every {{domxref("VRDisplay")}} object that is currently presenting ({{domxref("VRDisplay.ispresenting")}} is <code>true</code>).</dd>
 <dt>{{domxref("Navigator.getVRDisplays()")}}</dt>
 <dd>Returns a promise that resolves to an array of {{domxref("VRDisplay")}} objects representing any available VR displays connected to the computer.</dd>
</dl>

<h4 id="Window_events">Window events</h4>

<dl>
 <dt>{{domxref("Window.onvrdisplaypresentchange")}}</dt>
 <dd>Represents an event handler that will run when the presenting state of a VR display changes — i.e. goes from presenting to not presenting, or vice versa (when the {{event("vrdisplaypresentchange")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplayconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR display has been connected to the computer (when the {{event("vrdisplayconnect")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplaydisconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR display has been disconnected from the computer (when the {{event("vrdisplaydisconnect")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplayactivate")}}</dt>
 <dd>Represents an event handler that will run when a display is able to be presented to (when the {{event("vrdisplayactivate")}} event fires), for example if an HMD has been moved to bring it out of standby, or woken up by being put on.</dd>
 <dt>{{domxref("Window.onvrdisplaydeactivate")}}</dt>
 <dd>Represents an event handler that will run when a display can no longer be presented to (when the {{event("vrdisplaydeactivate")}} event fires), for example if an HMD has gone into standby or sleep mode due to a period of inactivity.</dd>
</dl>

<h4 id="Unimplemented_window_events">Unimplemented window events</h4>

<p>The following events are listed in the spec, but do not currently seem to be implemented anywhere as yet.</p>

<dl>
 <dt>{{domxref("Window.onvrdisplayblur")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has been paused for some reason by the browser, OS, or VR hardware (when the {{event("vrdisplayblur")}} event fires) — for example, while the user is interacting with a system menu or browser, to prevent tracking or loss of experience.</dd>
 <dt>{{domxref("Window.onvrdisplayfocus")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has resumed after being blurred (when the {{event("vrdisplayfocus")}} event fires).</dd>
</dl>

<h2 id="Examples">Examples</h2>

<p>You can find a number of examples at these locations:</p>

<ul>
 <li><a href="https://github.com/mdn/webvr-tests">webvr-tests</a> — very simple examples to accompany the MDN WebVR documentation.</li>
 <li><a href="https://github.com/facebook/Carmel-Starter-Kit">Carmel starter kit</a> — nice simple, well-commented examples that go along with Carmel, Facebook's WebVR browser.</li>
 <li><a href="https://webvr.info/samples/">WebVR.info samples</a> — slightly more in-depth examples plus source code</li>
 <li><a href="https://webvr.rocks/firefox#demos">WebVR.rocks Firefox demos</a> — showcase examples</li>
 <li><a href="https://aframe.io/">A-Frame homepage</a> — examples showing A-Frame usage</li>
</ul>

<h2 id="Specifications">Specifications</h2>

This API was specified in the old <a href="https://immersive-web.github.io/webvr/spec/1.1/">WebVR API</a> that has been superseded by the <a href="https://immersive-web.github.io/webxr/">WebXR Device API</a>. It is no longer on track to becoming a standard.

Until all browsers have implemented the new <a href="/zh-TW/docs/Web/API/WebXR_Device_API/Fundamentals">WebXR APIs</a>, it is recommended to rely on frameworks, like <a href="https://aframe.io/">A-Frame</a>, <a href="https://www.babylonjs.com/">Babylon.js</a>, or <a href="https://threejs.org/">Three.js</a>, or a <a href="https://github.com/immersive-web/webxr-polyfill">polyfill</a>, to develop WebXR applications that will work across all browsers <a href="https://developer.oculus.com/documentation/web/port-vr-xr/">[1]</a>.

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="https://vr.mozilla.org">vr.mozilla.org</a> — The main Mozilla landing pad for WebVR, with demos, utilities, and other information.</li>
 <li><a href="https://aframe.io/">A-Frame</a> — Open source web framework for building VR experiences.</li>
 <li><a href="https://webvr.info">webvr.info</a> — Up-to-date information about WebVR, browser setup, and community.</li>
 <li><a href="http://mozvr.com/">MozVr.com</a> — Demos, downloads, and other resources from the Mozilla VR team.</li>
 <li><a href="https://github.com/MozVR/vr-web-examples/tree/master/threejs-vr-boilerplate">threejs-vr-boilerplate</a> — A useful starter template for writing WebVR apps into.</li>
 <li><a href="https://github.com/googlevr/webvr-polyfill/">Web VR polyfill</a> — JavaScript implementation of WebVR.</li>
</ul>
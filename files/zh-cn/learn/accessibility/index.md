---
title: 可访问性
slug: learn/Accessibility
translation_of: Learn/Accessibility
---
# 可访问性

如果你想成为一个 web 开发者，学习一些 HTML,CSS 和 JavaScript 是很有用的，但是仅仅使用这些技术是不够的，你应该更进一步拓展你的知识 — 你需要响应式地使用它们来最大程度地发展你的用户，并且使用这些技术时不能把任何一门排斥出去。为了达到这个目的，要遵循一般最佳实践（这些最佳实践已经被 [HTML](/zh-CN/docs/Learn/HTML), [CSS](/zh-CN/docs/Learn/CSS), 和 [JavaScript](/zh-CN/docs/Learn/JavaScript) 相关的话题所证明）,进行跨浏览器测试，并且从项目最初阶段就把易使用性考虑在内。在这个模块中我们将会详细讨论后者。

## 预备知识：

为了充分理解这个模块，你至少需要读过 [HTML](/zh-CN/docs/Learn/HTML), [CSS](/zh-CN/docs/Learn/CSS), 和 [JavaScript](/zh-CN/docs/Learn/JavaScript) 各个话题的前两个模块，或者有可能的话，在你学习相关联的技术话题时也把可访问性相关的内容学习了，这样会更好。

> **备注：** 如果在你所使用的设备上你不能建立自己的文件，你可以使用在线编码平台运行大多数样例代码，比如 [JSBin](http://jsbin.com/) 或者 [Glitch](https://glitch.com/).

## 参考指南

- [什么是可访问性？](/zh-CN/docs/Learn/Accessibility/What_is_accessibility)
  - : 这篇文章开头很好地阐述了到底什么是'可访问性' — 这包括我们要考虑哪一群人以及为什么要考虑这些人，不同用户使用什么工具与网页交互，以及我们在网页开发流中如何构建可用性部分。
- [HTML: 确保可访问性的良好基础](/zh-CN/docs/Learn/Accessibility/HTML)
  - : 只要确保恰当的 HTML 元素被用于适当的目的， 大量的网页内容即可具有可用性，这篇文章详细地讲述了 HTML 的用法，以确保网页有最大的可访问性。
- [CSS 与 JavaScript 可用性最佳实践](/zh-CN/docs/Learn/Accessibility/CSS_and_JavaScript)
  - : CSS 与 JavaScript, 当正确使用的时候，也能够使得网页具有很好的可访问性，但是如果错误地使用他们将极大地破坏可访问性。这篇文章罗列了一些应该被考虑的 CSS 和 JavaScript 的最佳实践，确保再复杂的内容都可以有尽可能好的可访问性。
- [无障碍网页应用基础](/zh-CN/docs/Learn/Accessibility/WAI-ARIA_basics)
  - : 继上一篇文章之后，有时候制作复杂的 UI 控件会涉及到非语义的 HTML 和动态的 JavaScript 更新内容会很难。WAI-ARIA 是一种可以帮助解决这些问题的技术，通过增加浏览器和辅助技术可以识别和使用的进一步语义来让用户知道正在发生的事情。在这里，我们将展示如何在基本级别上使用它来提高可访问性。
- [多媒体](/zh-CN/docs/Learn/Accessibility/Multimedia)
  - : 可以提高可访问性的另一类内容是多媒体 - 视频，音频和图像内容需要提供适当的文本替代方案，以便辅助技术和相应的用户能够理解。这篇文章展示了永达。
- [移动设备可访问性](/zh-CN/docs/Learn/Accessibility/Mobile)
  - : 随着移动设备上网页访问的流行，以及主流平台（如 iOS 和 Android）具备了完善的辅助功能工具，考虑在这些平台上 Web 内容的可访问性也是非常重要的。本文讨论针对移动设备的可访问性注意事项。

## 评估

- [可访问性诊断](/zh-CN/docs/Learn/Accessibility/Accessibility_troubleshooting)
  - : 针对这篇模块，对于您的理解程度， 我们提供了评估方法，我们向您展示了一个简单的网站，其中包含许多您需要诊断和修复的可访问性问题。

## 另见

- [现在开始构建可访问性的 web 应用](https://egghead.io/courses/start-building-accessible-web-applications-today) — 来自 Marcy Sutton 的一系列优质的视频教程。
- [DequeUniversity 资源](https://dequeuniversity.com/resources/) — 包含代码示例，屏幕阅读参考和其他有用的资源。
- [WebAIM 资源](http://webaim.org/resources/) — 包含向导，清单，工具和其他资源。
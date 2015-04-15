## 手机浏览器下触发touchcancel事件的操作

Touchcancel事件在Javascript创建touch-interfaces时常常被忽视。而浏览器厂商也从未正式发布详细说明touchcancel事件何时会被触发的文档，因此，对于许多开发者而言touchcancel事件也鲜少被关注，了解touchcancel事件可以帮助我们解决开发中的难题，比如avalon的touch模块就充分利用touchcancel事件解决元素同时绑定tap和hold事件时都触发的问题

touch事件最初是Apple为Safari浏览器创建的，现在已经被纳入了W3C Touch 事件规范。原始的Safari DOM参考文档关于touchcancel事件的信息少的可怜，仅有一句话：

> 当系统取消跟踪touch事件时触发。

W3C Touch事件规范为其提供了更多细节，包括一些会触发touchcancel事件的场景:

> A user agent must dispatch this event type to indicate when a touch point has been disrupted in an implementation-specific manner, such as a synchronous event or action originating from the UA canceling the touch, or the touch point leaving the document window into a non-document area which is capable of handling user interactions. (e.g. The UA's native user interface, plug-ins) A user agent may also dispatch this event type when the user places more touch points on the touch surface than the device or implementation is configured to store, in which case the earliest Touch object in the TouchList should be removed.

[具体的描述可以参考此文](http://alxgbsn.co.uk/2011/12/23/different-ways-to-trigger-touchcancel-in-mobile-browsers/)

[touchcancel被触发的几种可能的原因](https://developer.mozilla.org/zh-CN/docs/Web/API/TouchEvent#touchcancel)







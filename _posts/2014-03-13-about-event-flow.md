---
layout: post
title: 事件之事件流
category: js
---
事件是用户或浏览器自身执行的某种动作。

##事件流

事件流描述的是从页面中接收事件的顺序

###1.事件冒泡

IE的事件叫事件冒泡，即事件开始时由最具体的元素接收，然后逐级向上传播到较为不具体的节点

div-->body-->html-->document

Firefox、Chrome、Safari将事件一直冒泡到window对象

### 2.事件捕获

不具体的节点更早接收到事件，而最具体的节点最后接收到事件，在事件到达预定目标之前捕获它

document-->html-->body-->div

Safari、Chrome、Opera和Firefox都支持这种事件流模型

### 3.DOM事件流

DOM2级事件规定的事件流包括三个阶段：

  事件捕获阶段-->处于目标阶段-->事件冒泡阶段。
  
首先发生的是事件捕获，为截获事件提供了机会。然后是实际的目标接收到事件。最后是冒泡阶段，可以在这个阶段对事件做出响应。

Opera、Firefox、Chrome、Safari都支持DOM事件流，IE不支持

---
title: "Aspose::Words::NodeChangingArgs 类"
linktitle: "NodeChangingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeChangingArgs 类。为 INodeChangingCallback 接口的方法提供数据。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


提供 [INodeChangingCallback](../inodechangingcallback/) 接口的方法所需的数据。欲了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class NodeChangingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Action](./get_action/)() const | 获取一个值，指示正在发生哪种类型的节点更改事件。 |
| [get_NewParent](./get_newparent/)() const | 获取操作完成后将被设置的节点父级。 |
| [get_Node](./get_node/)() const | 获取被添加或移除的 [Node](./get_node/)。 |
| [get_OldParent](./get_oldparent/)() const | 获取操作开始前的节点父级。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::INodeChangingCallback 接口"
linktitle: "INodeChangingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::INodeChangingCallback 接口。如果您希望在 C++ 中在文档的节点被插入或删除时接收通知，请实现此接口。"
type: docs
weight: 79000
url: /zh/cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


如果您希望在文档中节点被插入或删除时收到通知，请实现此接口。

```cpp
class INodeChangingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | 当属于此文档的节点已被插入到另一个节点时调用。 |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | 当属于此文档的节点即将被插入到另一个节点之前调用。 |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | 当属于此文档的节点已从其父节点中移除时调用。 |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | 当属于此文档的节点即将从文档中移除之前调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

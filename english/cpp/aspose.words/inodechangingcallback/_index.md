---
title: Aspose::Words::INodeChangingCallback interface
linktitle: INodeChangingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::INodeChangingCallback interface. Implement this interface if you want to receive notifications when nodes are inserted or removed in the document in C++.'
type: docs
weight: 79000
url: /cpp/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface


Implement this interface if you want to receive notifications when nodes are inserted or removed in the document.

```cpp
class INodeChangingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [NodeInserted](./nodeinserted/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Called when a node belonging to this document has been inserted into another node. |
| virtual [NodeInserting](./nodeinserting/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Called just before a node belonging to this document is about to be inserted into another node. |
| virtual [NodeRemoved](./noderemoved/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Called when a node belonging to this document has been removed from its parent. |
| virtual [NodeRemoving](./noderemoving/)(System::SharedPtr\<Aspose::Words::NodeChangingArgs\>) | Called just before a node belonging to this document is about to be removed from the document. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

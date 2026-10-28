---
title: Aspose::Words::NodeChangingArgs class
linktitle: NodeChangingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeChangingArgs class. Provides data for methods of the INodeChangingCallback interface. DocumentBaseINodeChangingCallbackNodeChangingActionTo learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words/nodechangingargs/
---
## NodeChangingArgs class


Provides data for methods of the [INodeChangingCallback](../inodechangingcallback/) interface. [DocumentBase](../documentbase/)[INodeChangingCallback](../inodechangingcallback/)[NodeChangingAction](../nodechangingaction/)
To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```cpp
class NodeChangingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_Action](./get_action/)() const | Gets a value indicating what type of node change event is occurring. |
| [get_NewParent](./get_newparent/)() const | Gets the node's parent that will be set after the operation completes. |
| [get_Node](./get_node/)() const | Gets the [Node](./get_node/) that is being added or removed. |
| [get_OldParent](./get_oldparent/)() const | Gets the node's parent before the operation began. |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)

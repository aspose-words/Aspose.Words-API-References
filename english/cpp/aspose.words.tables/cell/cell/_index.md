---
title: Aspose::Words::Tables::Cell::Cell constructor
linktitle: Cell
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell::Cell constructor. Initializes a new instance of the Cell class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.tables/cell/cell/
---
## Cell::Cell constructor


Initializes a new instance of the [Cell](../) class.

```cpp
Aspose::Words::Tables::Cell::Cell(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Cell](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [Cell](../) to the document use [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the row where you want the cell inserted.

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

---
title: Aspose::Words::Tables::Row::Row constructor
linktitle: Row
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Row::Row constructor. Initializes a new instance of the Row class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.tables/row/row/
---
## Row::Row constructor


Initializes a new instance of the [Row](../) class.

```cpp
Aspose::Words::Tables::Row::Row(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Row](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [Row](../) to the document use [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the table where you want the row inserted.

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

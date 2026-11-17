---
title: Aspose::Words::Tables::Table::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.tables/table/accept/
---
## Table::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::Tables::Table::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)

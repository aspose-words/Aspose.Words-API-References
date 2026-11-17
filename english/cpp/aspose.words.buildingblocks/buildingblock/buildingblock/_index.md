---
title: Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock constructor
linktitle: BuildingBlock
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.buildingblocks/buildingblock/buildingblock/
---
## BuildingBlock::BuildingBlock constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::BuildingBlocks::BuildingBlock::BuildingBlock(const System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> &glossaryDoc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| glossaryDoc | const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\& | The owner document. |
## Remarks


When [BuildingBlock](../) is created, it belongs to the specified glossary document, but is not yet part of the glossary document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [BuildingBlock](../) to a [GlossaryDocument](../../glossarydocument/) use [AppendChild``1()](../).

## See Also

* Class [GlossaryDocument](../../glossarydocument/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)

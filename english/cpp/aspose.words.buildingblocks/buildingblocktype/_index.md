---
title: Aspose::Words::BuildingBlocks::BuildingBlockType enum
linktitle: BuildingBlockType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlockType enum. Specifies a building block type. The type might affect the visibility and behavior of the building block in Microsoft Word in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enum


Specifies a building block type. The type might affect the visibility and behavior of the building block in Microsoft Word.

```cpp
enum class BuildingBlockType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No type information is specified for the building block. |
| AutomaticallyReplaceNameWithContent | 1 | Allows the building block to be automatically inserted into the document whenever its name is entered into an application. |
| StructuredDocumentTagPlaceholderText | 2 | The building block is a structured document tag placeholder text. |
| FormFieldHelpText | 3 | The building block is a form field help text. |
| Normal | 4 | The building block is a normal (i.e. regular) glossary document entry. |
| AutoCorrect | 5 | The building block is associated with the spelling and grammar tools. |
| AutoText | 6 | The building block is an AutoText entry. |
| All | 7 | The building block is associated with all types. |
| Default | n/a | Save as [None](./). |

## Remarks


Corresponds to the **ST_DocPartType** type in OOXML.

## See Also

* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)

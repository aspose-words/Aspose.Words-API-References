---
title: MoveToStructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: Moves the cursor to the structured document tag.
type: docs
weight: 742
url: /cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Moves the cursor to the structured document tag.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | The structured document tag to move to. |
| characterIndex | int32_t | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

## See Also

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Moves the cursor to a structured document tag in the current section.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | The index of the structured document tag to move to. |
| characterIndex | int32_t | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |
## Remarks


The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then structuredDocumentTagIndex specified the index of the structured document tag inside that header of that section.

When structuredDocumentTagIndex is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first structured document tag. When structuredDocumentTagIndex is less than 0, it specified an index from the end of the section with -1 being the last structured document tag.

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

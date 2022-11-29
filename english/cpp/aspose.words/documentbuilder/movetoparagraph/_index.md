---
title: MoveToParagraph
second_title: Aspose.Words for C++ API Reference
description: Moves the cursor to a paragraph in the current section.
type: docs
weight: 716
url: /cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Moves the cursor to a paragraph in the current section.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| paragraphIndex | int32_t | The index of the paragraph to move to. |
| characterIndex | int32_t | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |
## Remarks


The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then paragraphIndex specified the index of the paragraph inside that header of that section.

When paragraphIndex is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first paragraph. When paragraphIndex is less than 0, it specified an index from the end of the section with -1 being the last paragraph.

## Examples



Shows how to move a builder's cursor position to a specified paragraph. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");
SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Create document builder to edit the document. The builder's cursor,
// which is the point where it will insert new nodes when we call its document construction methods,
// is currently at the beginning of the document.
auto builder = MakeObject<DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Move that cursor to a different paragraph will place that cursor in front of that paragraph.
builder->MoveToParagraph(2, 0);

// Any new content that we add will be inserted at that point.
builder->Writeln(u"This is a new third paragraph. ");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)

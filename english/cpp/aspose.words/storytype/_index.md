---
title: StoryType
second_title: Aspose.Words for C++ API Reference
description: Text of a Word document is stored in stories. StoryType identifies a story.
type: docs
weight: 1522
url: /cpp/aspose.words/storytype/
---
## StoryType enum


Text of a Word document is stored in stories. [StoryType](./) identifies a story.

```cpp
enum class StoryType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Default value. There is no such story in the document. |
| MainText | 1 | Contains the main text of the document, represented by [Body](../body/). |
| Footnotes | 2 | Contains footnote text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Contains endnotes text, represented by [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Contains document comments (annotations), represented by [Comment](../comment/). |
| Textbox | 5 | Contains shape or textbox text, represented by [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Contains text of the even pages header, represented by [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Contains text of the primary header. When header is different for odd and even pages, contains text of the odd pages header. Represented by [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Contains text of the even pages footer, represented by [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Contains text of the primary footer. When footer is different for odd and even pages, contains text of the odd pages footer. Represented by [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Contains text of the first page header, represented by [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Contains text of the first page footer, represented by [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Contains the text of the footnote separator, represented by [FootnoteSeparator](../). |
| FootnoteContinuationSeparator | 13 | Contains the text of the footnote continuation separator, represented by [FootnoteSeparator](../). |
| FootnoteContinuationNotice | 14 | Contains the text of the footnote continuation notice separator, represented by [FootnoteSeparator](../). |
| EndnoteSeparator | 15 | Contains the text of the endnote separator, represented by [FootnoteSeparator](../). |
| EndnoteContinuationSeparator | 16 | Contains the text of the endnote continuation separator, represented by [FootnoteSeparator](../). |
| EndnoteContinuationNotice | 17 | Contains the text of the endnote continuation notice separator, represented by [FootnoteSeparator](../). |


## Examples



Shows how to remove all shapes from a node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder->InsertShape(ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(NodeType::Shape, true)->get_Count());

// We can delete all shapes from the child paragraphs of this Body.
ASSERT_EQ(StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)

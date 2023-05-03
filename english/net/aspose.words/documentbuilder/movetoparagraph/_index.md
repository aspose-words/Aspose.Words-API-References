---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder MoveToParagraph method. Moves the cursor to a paragraph in the current section in C#.
type: docs
weight: 560
url: /net/aspose.words/documentbuilder/movetoparagraph/
---
## MoveToParagraph method

Moves the cursor to a paragraph in the current section.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| paragraphIndex | Int32 | The index of the paragraph to move to. |
| characterIndex | Int32 | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |

## Remarks

The navigation is performed inside the current story of the current section. That is, if you moved the cursor to the primary header of the first section, then *paragraphIndex* specified the index of the paragraph inside that header of that section.

When *paragraphIndex* is greater than or equal to 0, it specifies an index from the beginning of the section with 0 being the first paragraph. When *paragraphIndex* is less than 0, it specified an index from the end of the section with -1 being the last paragraph.

## Examples

Shows how to move a builder's cursor position to a specified paragraph.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Create document builder to edit the document. The builder's cursor,
// which is the point where it will insert new nodes when we call its document construction methods,
// is currently at the beginning of the document.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Move that cursor to a different paragraph will place that cursor in front of that paragraph.
builder.MoveToParagraph(2, 0);
// Any new content that we add will be inserted at that point.
builder.Writeln("This is a new third paragraph. ");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---
title: DocumentBuilder.moveToParagraph method
linktitle: moveToParagraph method
articleTitle: moveToParagraph method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.moveToParagraph method. Moves the cursor to a paragraph in the current section."
type: docs
weight: 600
url: /nodejs-net/aspose.words/documentbuilder/moveToParagraph/
---

## moveToParagraph(paragraphIndex, characterIndex) {#number_number}

Moves the cursor to a paragraph in the current section.


```js
moveToParagraph(paragraphIndex: numbercharacterIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| paragraphIndex | number | The index of the paragraph to move to. |
| characterIndex | number | The index of the character inside the paragraph. A negative value allows you to specify a position from the end of the paragraph. Use -1 to move to the end of the paragraph. |

### Remarks

The navigation is performed inside the current story of the current section.
That is, if you moved the cursor to the primary header of the first section,
then *paragraphIndex* specified the index of the paragraph inside that header
of that section.

When *paragraphIndex* is greater than or equal to 0, it specifies an index from
the beginning of the section with 0 being the first paragraph. When*paragraphIndex* is less than 0,
it specified an index from the end of the section with -1 being the last paragraph.




### Examples

Shows how to move a builder's cursor position to a specified paragraph.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");
let paragraphs = doc.firstSection.body.paragraphs;

expect(paragraphs.count).toEqual(22);

// Create document builder to edit the document. The builder's cursor,
// which is the point where it will insert new nodes when we call its document construction methods,
// is currently at the beginning of the document.
let builder = new aw.DocumentBuilder(doc);

expect(paragraphs.indexOf(builder.currentParagraph)).toEqual(0);

// Move that cursor to a different paragraph will place that cursor in front of that paragraph.
builder.moveToParagraph(2, 0);
expect(paragraphs.indexOf(builder.currentParagraph)).toEqual(2);

// Any new content that we add will be inserted at that point.
builder.writeln("This is a new third paragraph. ");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)


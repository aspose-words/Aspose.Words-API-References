---
title: Story.appendParagraph method
linktitle: appendParagraph method
articleTitle: appendParagraph method
second_title: Aspose.Words for Node.js
description: "Story.appendParagraph method. A shortcut method that creates a [Paragraph](../../paragraph/) object with optional text and appends it to the end of this object."
type: docs
weight: 60
url: /nodejs-net/aspose.words/story/appendParagraph/
---

## appendParagraph(text) {#string}

A shortcut method that creates a [Paragraph](../../paragraph/) object with optional text and appends it to the end of this object.



```js
appendParagraph(text: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | The text for the paragraph. Can be ``null`` or empty string. |

### Returns

The newly created and appended paragraph.


### Examples

Shows how to create a header and a footer.

```js
let doc = new aw.Document();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
let header = new aw.HeaderFooter(doc, aw.HeaderFooterType.HeaderPrimary);
doc.firstSection.headersFooters.add(header);

let para = header.appendParagraph("My header.");

expect(header.isHeader).toEqual(true);
expect(para.isEndOfHeaderFooter).toEqual(true);

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
let footer = new aw.HeaderFooter(doc, aw.HeaderFooterType.FooterPrimary);
doc.firstSection.headersFooters.add(footer);

para = footer.appendParagraph("My footer.");

expect(footer.isHeader).toEqual(false);
expect(para.isEndOfHeaderFooter).toEqual(true);

expect(para.parentStory.referenceEquals(footer)).toEqual(true);
expect(para.parentSection.referenceEquals(footer.parentSection)).toEqual(true);
expect(header.parentSection.referenceEquals(footer.parentSection)).toEqual(true);

doc.save(base.artifactsDir + "HeaderFooter.create.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Story](../)


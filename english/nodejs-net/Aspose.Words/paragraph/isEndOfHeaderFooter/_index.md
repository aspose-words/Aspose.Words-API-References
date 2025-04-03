---
title: Paragraph.isEndOfHeaderFooter property
linktitle: isEndOfHeaderFooter property
articleTitle: isEndOfHeaderFooter property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isEndOfHeaderFooter property. True if this paragraph is the last paragraph in the [HeaderFooter](../../headerfooter/) (main text story) of a [Section](../../section/); false otherwise."
type: docs
weight: 70
url: /nodejs-net/aspose.words/paragraph/isEndOfHeaderFooter/
---

## Paragraph.isEndOfHeaderFooter property

True if this paragraph is the last paragraph in the [HeaderFooter](../../headerfooter/) (main text story) of a [Section](../../section/); false otherwise.



```js
get isEndOfHeaderFooter(): boolean
```

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
* class [Paragraph](../)


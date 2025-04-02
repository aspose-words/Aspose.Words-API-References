---
title: ParagraphFormat.pageBreakBefore property
linktitle: pageBreakBefore property
articleTitle: pageBreakBefore property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.pageBreakBefore property. True if a page break is forced before the paragraph."
type: docs
weight: 270
url: /nodejs-net/Aspose.Words/paragraphformat/pageBreakBefore/
---

## ParagraphFormat.pageBreakBefore property

True if a page break is forced before the paragraph.


```js
get pageBreakBefore(): boolean
```

### Examples

Shows how to create paragraphs with page breaks at the beginning.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set this flag to "true" to apply a page break to each paragraph's beginning
// that the document builder will create under this ParagraphFormat configuration.
// The first paragraph will not receive a page break.
// Leave this flag as "false" to start each new paragraph on the same page
// as the previous, provided there is sufficient space.
builder.paragraphFormat.pageBreakBefore = pageBreakBefore;

builder.writeln("Paragraph 1.");
builder.writeln("Paragraph 2.");

let layoutCollector = new aw.Layout.LayoutCollector(doc);
let paragraphs = doc.firstSection.body.paragraphs;

if (pageBreakBefore)
{
  expect(layoutCollector.getStartPageIndex(paragraphs.at(0))).toEqual(1);
  expect(layoutCollector.getStartPageIndex(paragraphs.at(1))).toEqual(2);
}
else
{
  expect(layoutCollector.getStartPageIndex(paragraphs.at(0))).toEqual(1);
  expect(layoutCollector.getStartPageIndex(paragraphs.at(1))).toEqual(1);
}

doc.save(base.artifactsDir + "ParagraphFormat.pageBreakBefore.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)


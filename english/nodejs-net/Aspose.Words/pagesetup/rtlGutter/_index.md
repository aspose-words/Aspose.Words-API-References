---
title: PageSetup.rtlGutter property
linktitle: rtlGutter property
articleTitle: rtlGutter property
second_title: Aspose.Words for NodeJs
description: "PageSetup.rtlGutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /nodejs-net/aspose.words/pagesetup/rtlGutter/
---

## PageSetup.rtlGutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```js
get rtlGutter(): boolean
```

### Examples

Shows how to set gutter margins.

```js
let doc = new aw.Document();

// Insert text that spans several pages.
let builder = new aw.DocumentBuilder(doc);
for (let i = 0; i < 6; i++)
{
  builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
        "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
  builder.insertBreak(aw.BreakType.PageBreak);
}

// A gutter adds whitespaces to either the left or right page margin,
// which makes up for the center folding of pages in a book encroaching on the page's layout.
let pageSetup = doc.sections.at(0).pageSetup;

// Determine how much space our pages have for text within the margins and then add an amount to pad a margin. 
expect(pageSetup.pageWidth - pageSetup.leftMargin - pageSetup.rightMargin).toEqual(468);

pageSetup.gutter = 100.0;

// Set the "RtlGutter" property to "true" to place the gutter in a more suitable position for right-to-left text.
pageSetup.rtlGutter = true;

// Set the "MultiplePages" property to "MultiplePagesType.MirrorMargins" to alternate
// the left/right page side position of margins every page.
pageSetup.multiplePages = aw.Settings.MultiplePagesType.MirrorMargins;

doc.save(base.artifactsDir + "PageSetup.gutter.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)


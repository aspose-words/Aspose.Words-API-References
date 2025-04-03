---
title: PageSetup.charactersPerLine property
linktitle: charactersPerLine property
articleTitle: charactersPerLine property
second_title: Aspose.Words for NodeJs
description: "PageSetup.charactersPerLine property. Gets or sets the number of characters per line in the document grid."
type: docs
weight: 100
url: /nodejs-net/aspose.words/pagesetup/charactersPerLine/
---

## PageSetup.charactersPerLine property

Gets or sets the number of characters per line in the document grid.


```js
get charactersPerLine(): number
```

### Remarks

Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal
style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters
per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal
style.




### Examples

Shows how to specify a for the number of characters that each line may have.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Enable pitching, and then use it to set the number of characters per line in this section.
builder.pageSetup.layoutMode = aw.SectionLayoutMode.Grid;
builder.pageSetup.charactersPerLine = 10;

// The number of characters also depends on the size of the font.
doc.styles.at("Normal").font.size = 20;

expect(doc.firstSection.pageSetup.charactersPerLine).toEqual(8);

builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.save(base.artifactsDir + "PageSetup.charactersPerLine.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)


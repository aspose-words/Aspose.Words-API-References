---
title: PageSetup.layoutMode property
linktitle: layoutMode property
articleTitle: layoutMode property
second_title: Aspose.Words for NodeJs
description: "PageSetup.layoutMode property. Gets or sets the layout mode of this section."
type: docs
weight: 190
url: /nodejs-net/Aspose.Words/pagesetup/layoutMode/
---

## PageSetup.layoutMode property

Gets or sets the layout mode of this section.


```js
get layoutMode(): Aspose.Words.SectionLayoutMode
```

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

Shows how to specify a limit for the number of lines that each page may have.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Enable pitching, and then use it to set the number of lines per page in this section.
// A large enough font size will push some lines down onto the next page to avoid overlapping characters.
builder.pageSetup.layoutMode = aw.SectionLayoutMode.LineGrid;
builder.pageSetup.linesPerPage = 15;

builder.paragraphFormat.snapToGrid = true;

for (let i = 0; i < 30; i++)
  builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.save(base.artifactsDir + "PageSetup.linesPerPage.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)


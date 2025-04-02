---
title: PageSetup.linesPerPage property
linktitle: linesPerPage property
articleTitle: linesPerPage property
second_title: Aspose.Words for NodeJs
description: "PageSetup.linesPerPage property. Gets or sets the number of lines per page in the document grid."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words/pagesetup/linesPerPage/
---

## PageSetup.linesPerPage property

Gets or sets the number of lines per page in the document grid.


```js
get linesPerPage(): number
```

### Remarks

Minimum value of the property is 1. Maximum value depends on page height and font size of the Normal
style. Minimum line pitch is 136 percent of the font size. For example, maximum number of lines per page of
a Letter page with one-inch margins is 39.

By default, the property has a value, on which line pitch is in 1.5 times greater than font size of
the Normal style.




### Examples

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


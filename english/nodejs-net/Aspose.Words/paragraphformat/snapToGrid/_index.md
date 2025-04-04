---
title: ParagraphFormat.snapToGrid property
linktitle: snapToGrid property
articleTitle: snapToGrid property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.snapToGrid property. Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph."
type: docs
weight: 300
url: /nodejs-net/aspose.words/paragraphformat/snapToGrid/
---

## ParagraphFormat.snapToGrid property

Specifies whether the current paragraph should use the document grid lines per page settings
when laying out the contents in the paragraph.


```js
get snapToGrid(): boolean
```

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
* class [ParagraphFormat](../)


---
title: SectionLayoutMode enumeration
linktitle: SectionLayoutMode enumeration
articleTitle: SectionLayoutMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.SectionLayoutMode enumeration. Specifies the layout mode for a section allowing to define the document grid behavior."
type: docs
weight: 1190
url: /nodejs-net/aspose.words/sectionlayoutmode/
---

## SectionLayoutMode enumeration

Specifies the layout mode for a section allowing to define the document grid behavior.


### Members

| Name | Description |
| --- | --- |
| Default | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| Grid | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing. |
| LineGrid | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| SnapToChars | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line.  Characters will be automatically aligned with gridlines on typing. |

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

* module [Aspose.Words](../)


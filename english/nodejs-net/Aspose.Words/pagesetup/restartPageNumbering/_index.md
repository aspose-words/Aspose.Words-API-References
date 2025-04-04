---
title: PageSetup.restartPageNumbering property
linktitle: restartPageNumbering property
articleTitle: restartPageNumbering property
second_title: Aspose.Words for Node.js
description: "PageSetup.restartPageNumbering property. True if page numbering restarts at the beginning of the section."
type: docs
weight: 360
url: /nodejs-net/aspose.words/pagesetup/restartPageNumbering/
---

## PageSetup.restartPageNumbering property

True if page numbering restarts at the beginning of the section.


```js
get restartPageNumbering(): boolean
```

### Remarks

If set to ``false``, the [PageSetup.restartPageNumbering](./) property will override the
[PageSetup.pageStartingNumber](../pageStartingNumber/) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Section 1, page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 1, page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 1, page 3.");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.writeln("Section 2, page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 2, page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Section 2, page 3.");

// Move the document builder to the first section's primary header,
// which every page in that section will display.
builder.moveToSection(0);
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);

// Insert a PAGE field, which will display the number of the current page.
builder.write("Page ");
builder.insertField("PAGE", "");

// Configure the section to have the page count that PAGE fields display start from 5.
// Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.restartPageNumbering = true;
pageSetup.pageStartingNumber = 5;
pageSetup.pageNumberStyle = aw.NumberStyle.UppercaseRoman;

// Create another primary header for the second section, with another PAGE field.
builder.moveToSection(1);
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.write(" - ");
builder.insertField("PAGE", "");
builder.write(" - ");

// Configure the section to have the page count that PAGE fields display start from 10.
// Also, configure all PAGE fields to display their page numbers using Arabic numbers.
pageSetup = doc.sections.at(1).pageSetup;
pageSetup.pageStartingNumber = 10;
pageSetup.restartPageNumbering = true;
pageSetup.pageNumberStyle = aw.NumberStyle.Arabic;

doc.save(base.artifactsDir + "PageSetup.PageNumbering.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)


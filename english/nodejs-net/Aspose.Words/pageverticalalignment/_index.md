---
title: PageVerticalAlignment enumeration
linktitle: PageVerticalAlignment enumeration
articleTitle: PageVerticalAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.PageVerticalAlignment enumeration. Specifies vertical justification of text on each page."
type: docs
weight: 970
url: /nodejs-net/aspose.words/pageverticalalignment/
---

## PageVerticalAlignment enumeration

Specifies vertical justification of text on each page.


### Members

| Name | Description |
| --- | --- |
| Bottom | Text is aligned at the bottom of the page. |
| Center | Text is aligned in the middle of the page. |
| Justify | Text is spread to fill the page. |
| Top | Text is aligned at the top of the page. |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Modify the page setup properties for the builder's current section and add text.
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.verticalAlignment = aw.PageVerticalAlignment.Center;
builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

// If we start a new section using a document builder,
// it will inherit the builder's current page setup properties.
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Landscape);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Center);

// We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.pageSetup.clearFormatting();

expect(doc.sections.at(1).pageSetup.orientation).toEqual(aw.Orientation.Portrait);
expect(doc.sections.at(1).pageSetup.verticalAlignment).toEqual(aw.PageVerticalAlignment.Top);

builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.save(base.artifactsDir + "PageSetup.clearFormatting.docx");
```

### See Also

* module [Aspose.Words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.verticalAlignment](../pagesetup/verticalAlignment/)


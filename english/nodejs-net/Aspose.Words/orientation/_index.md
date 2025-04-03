---
title: Orientation enumeration
linktitle: Orientation enumeration
articleTitle: Orientation enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Orientation enumeration. Specifies page orientation."
type: docs
weight: 920
url: /nodejs-net/aspose.words/orientation/
---

## Orientation enumeration

Specifies page orientation.


### Members

| Name | Description |
| --- | --- |
| Portrait | Portrait page orientation (narrow and tall). |
| Landscape | Landscape page orientation (wide and short). |

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


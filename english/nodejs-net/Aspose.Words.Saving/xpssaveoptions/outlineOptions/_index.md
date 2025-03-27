---
title: XpsSaveOptions.outlineOptions property
linktitle: outlineOptions property
articleTitle: outlineOptions property
second_title: Aspose.Words for NodeJs
description: "XpsSaveOptions.outlineOptions property. Allows to specify outline options."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/xpssaveoptions/outlineOptions/
---

## XpsSaveOptions.outlineOptions property

Allows to specify outline options.


```js
get outlineOptions(): Aspose.Words.Saving.OutlineOptions
```

### Remarks

Note that [OutlineOptions.expandedOutlineLevels](../../outlineoptions/expandedOutlineLevels/) option will not work when saving to XPS.




### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

expect(builder.paragraphFormat.isHeading).toEqual(true);

builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;

builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;

builder.writeln("Heading 1.2.1");
builder.writeln("Heading 1.2.2");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
let saveOptions = new aw.Saving.XpsSaveOptions();

expect(saveOptions.saveFormat).toEqual(aw.SaveFormat.Xps);

// The output XPS document will contain an outline, a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions.outlineOptions.headingsOutlineLevels = 2;

doc.save(base.artifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XpsSaveOptions](../)


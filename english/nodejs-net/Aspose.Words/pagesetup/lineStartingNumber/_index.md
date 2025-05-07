---
title: PageSetup.lineStartingNumber property
linktitle: lineStartingNumber property
articleTitle: lineStartingNumber property
second_title: Aspose.Words for Node.js
description: "PageSetup.lineStartingNumber property. Gets or sets the starting line number."
type: docs
weight: 240
url: /nodejs-net/aspose.words/pagesetup/lineStartingNumber/
---

## PageSetup.lineStartingNumber property

Gets or sets the starting line number.


```js
get lineStartingNumber(): number
```

### Examples

Shows how to enable line numbering for a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// We can use the section's PageSetup object to display numbers to the left of the section's text lines.
// This is the same behavior as a List object,
// but it covers the entire section and does not modify the text in any way.
// Our section will restart the numbering on each new page from 1 and display the number,
// if it is a multiple of 3, at 50pt to the left of the line.
let pageSetup = builder.pageSetup;
pageSetup.lineStartingNumber = 1;
pageSetup.lineNumberCountBy = 3;
pageSetup.lineNumberRestartMode = aw.LineNumberRestartMode.RestartPage;
pageSetup.lineNumberDistanceFromText = 50.0;

for (let i = 1; i <= 25; i++)
  builder.writeln(`Line ${i}.`);

// The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
// This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
// The section's line counter will also ignore this line, treat the next line as the 15th,
// and continue the count from that point onward.
doc.firstSection.body.paragraphs.at(14).paragraphFormat.suppressLineNumbers = true;

doc.save(base.artifactsDir + "PageSetup.LineNumbers.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)


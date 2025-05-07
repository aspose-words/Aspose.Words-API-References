---
title: ParagraphFormat.suppressLineNumbers property
linktitle: suppressLineNumbers property
articleTitle: suppressLineNumbers property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.suppressLineNumbers property. Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section."
type: docs
weight: 390
url: /nodejs-net/aspose.words/paragraphformat/suppressLineNumbers/
---

## ParagraphFormat.suppressLineNumbers property

Specifies whether the current paragraph's lines should be exempted from line numbering
which is applied in the parent section.


```js
get suppressLineNumbers(): boolean
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
* class [ParagraphFormat](../)


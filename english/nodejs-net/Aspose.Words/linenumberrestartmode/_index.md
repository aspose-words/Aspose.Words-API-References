---
title: LineNumberRestartMode enumeration
linktitle: LineNumberRestartMode enumeration
articleTitle: LineNumberRestartMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.LineNumberRestartMode enumeration. Determines when automatic line numbering restarts."
type: docs
weight: 750
url: /nodejs-net/aspose.words/linenumberrestartmode/
---

## LineNumberRestartMode enumeration

Determines when automatic line numbering restarts.


### Members

| Name | Description |
| --- | --- |
| RestartPage | Line numbering restarts at the start of every page. |
| RestartSection | Line numbering restarts at the section start. |
| Continuous | Line numbering continuous from the previous section. |

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

* module [Aspose.Words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.lineNumberRestartMode](../pagesetup/lineNumberRestartMode/)


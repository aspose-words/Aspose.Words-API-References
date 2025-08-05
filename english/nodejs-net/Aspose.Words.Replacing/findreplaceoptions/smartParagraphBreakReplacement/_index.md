---
title: FindReplaceOptions.smartParagraphBreakReplacement property
linktitle: smartParagraphBreakReplacement property
articleTitle: smartParagraphBreakReplacement property
second_title: Aspose.Words for Node.js
description: "FindReplaceOptions.smartParagraphBreakReplacement property. Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph."
type: docs
weight: 180
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/smartParagraphBreakReplacement/
---

## FindReplaceOptions.smartParagraphBreakReplacement property

Gets or sets a boolean value indicating either it is allowed to replace paragraph break
when there is no next sibling paragraph.

The default value is ``false``.




```js
get smartParagraphBreakReplacement(): boolean
```

### Remarks

This option allows to replace paragraph break when there is no next sibling paragraph to which all child
nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.


### Examples

Shows how to remove paragraph from a table cell with a nested table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create table with paragraph and inner table in first cell.
builder.startTable();
builder.insertCell();
builder.write("TEXT1");
builder.startTable();
builder.insertCell();
builder.endTable();
builder.endTable();
builder.writeln();

let options = new aw.Replacing.FindReplaceOptions();
// When the following option is set to 'true', Aspose.words will remove paragraph's text
// completely with its paragraph mark. Otherwise, Aspose.words will mimic Word and remove
// only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
options.smartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.range.replace(new Regex("TEXT1&p"), "", options);

doc.save(base.artifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


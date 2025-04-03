---
title: FindReplaceOptions.ignoreInserted property
linktitle: ignoreInserted property
articleTitle: ignoreInserted property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreInserted property. Gets or sets a boolean value indicating either to ignore text inside insert revisions"
type: docs
weight: 100
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/ignoreInserted/
---

## FindReplaceOptions.ignoreInserted property

Gets or sets a boolean value indicating either to ignore text inside insert revisions.
The default value is ``false``.



```js
get ignoreInserted(): boolean
```

### Examples

Shows how to include or ignore text inside insert revisions during a find-and-replace operation.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

// Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
doc.startTrackRevisions("John Doe", Date.now());
builder.writeln("Hello again!");
doc.stopTrackRevisions();

expect(doc.firstSection.body.paragraphs.at(1).isInsertRevision).toEqual(true);

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "IgnoreInserted" flag to "true" to get the find-and-replace
// operation to ignore paragraphs that are insert revisions.
// Set the "IgnoreInserted" flag to "false" to get the find-and-replace
// operation to also search for text inside insert revisions.
options.ignoreInserted = ignoreTextInsideInsertRevisions;

doc.range.replace("Hello", "Greetings", options);

expect(doc.getText().trim()).toEqual(
  ignoreTextInsideInsertRevisions
    ? "Greetings world!\rHello again!"
    : "Greetings world!\rGreetings again!");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


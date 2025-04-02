---
title: FindReplaceOptions.ignoreDeleted property
linktitle: ignoreDeleted property
articleTitle: ignoreDeleted property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreDeleted property. Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreDeleted/
---

## FindReplaceOptions.ignoreDeleted property

Gets or sets a boolean value indicating either to ignore text inside delete revisions.
The default value is ``False``.



```js
get ignoreDeleted(): boolean
```

### Examples

Shows how to include or ignore text inside delete revisions during a find-and-replace operation.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
builder.writeln("Hello again!");

// Start tracking revisions and remove the second paragraph, which will create a delete revision.
// That paragraph will persist in the document until we accept the delete revision.
doc.startTrackRevisions("John Doe", Date.now());
doc.firstSection.body.paragraphs.at(1).remove();
doc.stopTrackRevisions();

expect(doc.firstSection.body.paragraphs.at(1).isDeleteRevision).toEqual(true);

// We can use a "FindReplaceOptions" object to modify the find and replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
// operation to ignore paragraphs that are delete revisions.
// Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
// operation to also search for text inside delete revisions.
options.ignoreDeleted = ignoreTextInsideDeleteRevisions;

doc.range.replace("Hello", "Greetings", options);

expect(doc.getText().trim()).toEqual(
  ignoreTextInsideDeleteRevisions ? "Greetings world!\rHello again!" : "Greetings world!\rGreetings again!");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


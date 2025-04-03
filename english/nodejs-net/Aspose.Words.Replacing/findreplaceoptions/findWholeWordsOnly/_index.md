---
title: FindReplaceOptions.findWholeWordsOnly property
linktitle: findWholeWordsOnly property
articleTitle: findWholeWordsOnly property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.findWholeWordsOnly property. True indicates the oldValue must be a standalone word."
type: docs
weight: 50
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/findWholeWordsOnly/
---

## FindReplaceOptions.findWholeWordsOnly property

True indicates the oldValue must be a standalone word.


```js
get findWholeWordsOnly(): boolean
```

### Examples

Shows how to toggle standalone word-only find-and-replace operations.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options.findWholeWordsOnly = findWholeWordsOnly;

doc.range.replace("Jackson", "Louis", options);

expect(doc.getText().trim()).toEqual(
  findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville." );
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


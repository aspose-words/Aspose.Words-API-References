---
title: FindReplaceOptions.matchCase property
linktitle: matchCase property
articleTitle: matchCase property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.matchCase property. True indicates case-sensitive comparison, false indicates case-insensitive comparison."
type: docs
weight: 140
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/matchCase/
---

## FindReplaceOptions.matchCase property

True indicates case-sensitive comparison, false indicates case-insensitive comparison.


```js
get matchCase(): boolean
```

### Examples

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options.matchCase = matchCase;

doc.range.replace("Ruby", "Jade", options);

expect(doc.getText().trim()).toEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


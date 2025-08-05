---
title: FindReplaceOptions.useSubstitutions property
linktitle: useSubstitutions property
articleTitle: useSubstitutions property
second_title: Aspose.Words for Node.js
description: "FindReplaceOptions.useSubstitutions property. Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns"
type: docs
weight: 200
url: /nodejs-net/aspose.words.replacing/findreplaceoptions/useSubstitutions/
---

## FindReplaceOptions.useSubstitutions property

Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns.
The default value is ``false``.



```js
get useSubstitutions(): boolean
```

### Remarks

For the details on substitution elements please refer to:
https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.


### Examples

Shows how to replace the text with substitutions.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("John sold a car to Paul.");
builder.writeln("Jane sold a house to Joe.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "UseSubstitutions" property to "true" to get
// the find-and-replace operation to recognize substitution elements.
// Set the "UseSubstitutions" property to "false" to ignore substitution elements.
options.useSubstitutions = useSubstitutions;

/* TODO
let regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.range.replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
  useSubstitutions
    ? "Paul bought a car from John.\rJoe bought a house from Jane."
    : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.getText().trim()); */
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)


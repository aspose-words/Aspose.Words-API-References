---
title: Granularity enumeration
linktitle: Granularity enumeration
articleTitle: Granularity enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Comparing.Granularity enumeration. Specifies the granularity of changes to track when comparing two documents."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Comparing/granularity/
---

## Granularity enumeration

Specifies the granularity of changes to track when comparing two documents.


### Members

| Name | Description |
| --- | --- |
| CharLevel | Specifies changes at the character level. |
| WordLevel | Specifies changes at the word level. |

### Examples

Shows to specify a granularity while comparing documents.

```js
let docA = new aw.Document();
let builderA = new aw.DocumentBuilder(docA);
builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

let docB = new aw.Document();
let builderB = new aw.DocumentBuilder(docB);
builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specify whether changes are tracking
// by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
Aspose.words.Comparing.CompareOptions compareOptions = new Aspose.words.Comparing.CompareOptions();
compareOptions.granularity = granularity;

docA.compare(docB, "author", Date.now(), compareOptions);

// The first document's collection of revision groups contains all the differences between documents.
let groups = docA.revisions.groups;
expect(groups.count).toEqual(5);
```

### See Also

* module [Aspose.Words.Comparing](../)


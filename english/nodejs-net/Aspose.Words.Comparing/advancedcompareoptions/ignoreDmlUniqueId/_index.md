---
title: AdvancedCompareOptions.ignoreDmlUniqueId property
linktitle: ignoreDmlUniqueId property
articleTitle: ignoreDmlUniqueId property
second_title: Aspose.Words for Node.js
description: "AdvancedCompareOptions.ignoreDmlUniqueId property. Specifies whether to ignore difference in DrawingML unique Id."
type: docs
weight: 20
url: /nodejs-net/aspose.words.comparing/advancedcompareoptions/ignoreDmlUniqueId/
---

## AdvancedCompareOptions.ignoreDmlUniqueId property

Specifies whether to ignore difference in DrawingML unique Id.


```js
get ignoreDmlUniqueId(): boolean
```

### Remarks

Default value is ``false``.



### Examples

Shows how to compare documents ignoring DML unique ID.

```js
let docA = new aw.Document(base.myDir + "DML unique ID original.docx");
let docB = new aw.Document(base.myDir + "DML unique ID compare.docx");

// By default, Aspose.words do not ignore DML's unique ID, and the revisions count was 2.
// If we are ignoring DML's unique ID, and revisions count were 0.
let compareOptions = new aw.Comparing.CompareOptions();
compareOptions.advancedOptions.ignoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.compare(docB, "Aspose.words", Date.now(), compareOptions);

expect(docA.revisions.count).toEqual(isIgnoreDmlUniqueId ? 0 : 2);
```

### See Also

* module [Aspose.Words.Comparing](../../)
* class [AdvancedCompareOptions](../)


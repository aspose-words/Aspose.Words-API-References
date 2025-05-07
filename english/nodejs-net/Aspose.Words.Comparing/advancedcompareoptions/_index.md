---
title: AdvancedCompareOptions class
linktitle: AdvancedCompareOptions class
articleTitle: AdvancedCompareOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Comparing.AdvancedCompareOptions class. Allows to set advanced compare options."
type: docs
weight: 10
url: /nodejs-net/aspose.words.comparing/advancedcompareoptions/
---

## AdvancedCompareOptions class

Allows to set advanced compare options.


### Remarks

These options have no equivalence in Microsoft Word and might help to produce more precise comparison result.


### Constructors
| Name | Description |
| --- | --- |
| [AdvancedCompareOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [ignoreDmlUniqueId](./ignoreDmlUniqueId/) | Specifies whether to ignore difference in DrawingML unique Id. |
| [ignoreStoreItemId](./ignoreStoreItemId/) | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |

### Examples

Shows how to compare SDT with same content but different store item id.

```js
let docA = new aw.Document(base.myDir + "Document with SDT 1.docx");
let docB = new aw.Document(base.myDir + "Document with SDT 2.docx");

// Configure options to compare SDT with same content but different store item id.
let compareOptions = new aw.Comparing.CompareOptions();
compareOptions.advancedOptions.ignoreStoreItemId = false;

docA.compare(docB, "user", Date.now(), compareOptions);
expect(docA.revisions.count).toEqual(8);

compareOptions.advancedOptions.ignoreStoreItemId = true;

docA.revisions.rejectAll();
docA.compare(docB, "user", Date.now(), compareOptions);
expect(docA.revisions.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Comparing](../)


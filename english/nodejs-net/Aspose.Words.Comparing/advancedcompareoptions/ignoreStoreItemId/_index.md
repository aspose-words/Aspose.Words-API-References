---
title: AdvancedCompareOptions.ignoreStoreItemId property
linktitle: ignoreStoreItemId property
articleTitle: ignoreStoreItemId property
second_title: Aspose.Words for NodeJs
description: "AdvancedCompareOptions.ignoreStoreItemId property. Specifies whether to ignore difference in StructuredDocumentTag store item Id."
type: docs
weight: 30
url: /nodejs-net/aspose.words.comparing/advancedcompareoptions/ignoreStoreItemId/
---

## AdvancedCompareOptions.ignoreStoreItemId property

Specifies whether to ignore difference in StructuredDocumentTag store item Id.


```js
get ignoreStoreItemId(): boolean
```

### Remarks

Default value is ``false``.



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

* module [Aspose.Words.Comparing](../../)
* class [AdvancedCompareOptions](../)


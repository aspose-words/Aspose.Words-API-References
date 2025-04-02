---
title: StyleCollection.clearQuickStyleGallery method
linktitle: clearQuickStyleGallery method
articleTitle: clearQuickStyleGallery method
second_title: Aspose.Words for NodeJs
description: "StyleCollection.clearQuickStyleGallery method. Removes all styles from the Quick Style Gallery panel."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/stylecollection/clearQuickStyleGallery/
---

## clearQuickStyleGallery() {#default}

Removes all styles from the Quick Style Gallery panel.


```js
clearQuickStyleGallery()
```

### Examples

Shows how to remove styles from Style Gallery panel.

```js
let doc = new aw.Document();
// Note that remove styles work only with DOCX format for now.
doc.styles.clearQuickStyleGallery();

doc.save(base.artifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [StyleCollection](../)


---
title: TxtLoadOptions.auto_numbering_detection property
linktitle: auto_numbering_detection property
articleTitle: auto_numbering_detection property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.auto_numbering_detection property. Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document"
type: docs
weight: 20
url: /python-net/aspose.words.loading/txtloadoptions/auto_numbering_detection/
---

## TxtLoadOptions.auto_numbering_detection property

Gets or sets a boolean value indicating either automatic numbering detection
will be performed while loading a document.
The default value is ``True``.



### Examples

Shows how to disable automatic numbering detection.

```python
options = aw.loading.TxtLoadOptions()
options.auto_numbering_detection = False
doc = aw.Document(MY_DIR + "Number detection.txt", options)
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)


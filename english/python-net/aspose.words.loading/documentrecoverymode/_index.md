---
title: DocumentRecoveryMode enumeration
linktitle: DocumentRecoveryMode enumeration
articleTitle: DocumentRecoveryMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentRecoveryMode enumeration. Specifies the available recovery options when a document encounters errors during loading."
type: docs
weight: 50
url: /python-net/aspose.words.loading/documentrecoverymode/
---

## DocumentRecoveryMode enumeration

Specifies the available recovery options when a document encounters errors during loading.


### Members

| Name | Description |
| --- | --- |
| NONE | No recovery is attempted.   If the document is invalid, loading will fail with an error. |
| TRY_RECOVER | Attempts to recover the document while preserving as much data as possible. |

### Examples

Shows how to try to recover a document if errors occurred during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.recovery_mode = aw.loading.DocumentRecoveryMode.TRY_RECOVER
doc = aw.Document(file_name=MY_DIR + 'Corrupted footnotes.docx', load_options=load_options)
```

### See Also

* module [aspose.words.loading](../)


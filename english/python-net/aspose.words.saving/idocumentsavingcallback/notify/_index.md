---
title: notify method
second_title: Aspose.Words for Python via .NET API Reference
description: "This is called to notify of document saving progress."
type: docs
weight: 10
url: /python-net/aspose.words.saving/idocumentsavingcallback/notify/
---

## notify(args) {#documentsavingargs}

This is called to notify of document saving progress.


```python
def notify(self, args: aspose.words.saving.DocumentSavingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentSavingArgs](../../documentsavingargs/) |  |

The primary uses for this interface is to allow application code to obtain progress status and abort saving process.


An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.




### See Also

* module [aspose.words.saving](../../)
* class [IDocumentSavingCallback](../)


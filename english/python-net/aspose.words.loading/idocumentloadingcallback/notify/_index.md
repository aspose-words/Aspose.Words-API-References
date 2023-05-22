---
title: IDocumentLoadingCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for Python
description: "IDocumentLoadingCallback.notify method. This is called to notify of document loading progress."
type: docs
weight: 10
url: /python-net/aspose.words.loading/idocumentloadingcallback/notify/
---

## notify(args) {#documentloadingargs}

This is called to notify of document loading progress.


```python
def notify(self, args: aspose.words.loading.DocumentLoadingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../documentloadingargs/) |  |

The primary uses for this interface is to allow application code to obtain progress status and abort loading process.


An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.




### See Also

* module [aspose.words.loading](../../)
* class [IDocumentLoadingCallback](../)
* property [LoadOptions.progress_callback](../../loadoptions/progress_callback/)


---
title: IDocumentLoadingCallback class
linktitle: IDocumentLoadingCallback class
articleTitle: IDocumentLoadingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.loading.IDocumentLoadingCallback class. Implement this interface if you want to have your own custom method called during loading a document."
type: docs
weight: 90
url: /python-net/aspose.words.loading/idocumentloadingcallback/
---

## IDocumentLoadingCallback class

Implement this interface if you want to have your own custom method called during loading a document.


### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#documentloadingargs) | This is called to notify of document loading progress. |

### Examples

Shows how to notify the user if document loading exceeded expected loading time (LoadingProgressCallback).

```python
class LoadingProgressCallback(aw.loading.IDocumentLoadingCallback):

    def __init__(self):
        self.max_duration = 0.5
        self.m_loading_started_at = datetime.datetime.now()

    def notify(self, args):
        from datetime import datetime
        canceled_at = datetime.now()
        elapsed_seconds = (canceled_at - self.loading_started_at).total_seconds()
        if elapsed_seconds > self.max_duration:
            raise Exception()
```

### See Also

* module [aspose.words.loading](../)


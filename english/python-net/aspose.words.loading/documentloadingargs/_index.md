---
title: DocumentLoadingArgs class
linktitle: DocumentLoadingArgs class
articleTitle: DocumentLoadingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.loading.DocumentLoadingArgs class. An argument passed into [IDocumentLoadingCallback.notify()](../idocumentloadingcallback/notify/#documentloadingargs)"
type: docs
weight: 40
url: /python-net/aspose.words.loading/documentloadingargs/
---

## DocumentLoadingArgs class

An argument passed into [IDocumentLoadingCallback.notify()](../idocumentloadingcallback/notify/#documentloadingargs).
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [estimated_progress](./estimated_progress/) | Overall estimated percentage progress. |

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


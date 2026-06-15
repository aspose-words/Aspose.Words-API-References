---
title: DocumentLoadingArgs.estimated_progress property
linktitle: estimated_progress property
articleTitle: estimated_progress property
second_title: Aspose.Words for Python
description: "DocumentLoadingArgs.estimated_progress property. Overall estimated percentage progress."
type: docs
weight: 10
url: /python-net/aspose.words.loading/documentloadingargs/estimated_progress/
---

## DocumentLoadingArgs.estimated_progress property

Overall estimated percentage progress.


```python
@property
def estimated_progress(self) -> float:
    ...

```

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

* module [aspose.words.loading](../../)
* class [DocumentLoadingArgs](../)


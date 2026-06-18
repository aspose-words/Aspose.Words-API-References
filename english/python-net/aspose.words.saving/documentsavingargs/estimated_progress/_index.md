---
title: DocumentSavingArgs.estimated_progress property
linktitle: estimated_progress property
articleTitle: estimated_progress property
second_title: Aspose.Words for Python
description: "DocumentSavingArgs.estimated_progress property. Overall estimated percentage progress."
type: docs
weight: 10
url: /python-net/aspose.words.saving/documentsavingargs/estimated_progress/
---

## DocumentSavingArgs.estimated_progress property

Overall estimated percentage progress.


```python
@property
def estimated_progress(self) -> float:
    ...

```

### Examples

Shows how to manage a document while saving to html (SavingProgressCallback).

```python
class SavingProgressCallback(aw.saving.IDocumentSavingCallback):

    def __init__(self):
        self.max_duration = 0.1
        self.m_saving_started_at = datetime.datetime.now()

    def notify(self, args):
        canceled_at = datetime.datetime.now()
        elapsed_seconds = (canceled_at - m_saving_started_at).total_seconds()
        if elapsed_seconds > self.max_duration:
            raise Exception()
```

Shows how to manage a document while saving to docx (SavingProgressCallback).

```python
class SavingProgressCallback(aw.saving.IDocumentSavingCallback):

    def __init__(self):
        self.max_duration = 0.01
        self.m_saving_started_at = datetime.datetime.now()

    def notify(self, args):
        canceled_at = datetime.datetime.now()
        elapsed_seconds = (canceled_at - m_saving_started_at).total_seconds()
        if elapsed_seconds > self.max_duration:
            raise Exception()
```

### See Also

* module [aspose.words.saving](../../)
* class [DocumentSavingArgs](../)


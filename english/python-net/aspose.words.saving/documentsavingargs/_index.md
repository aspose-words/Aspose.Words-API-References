---
title: DocumentSavingArgs class
linktitle: DocumentSavingArgs class
articleTitle: DocumentSavingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocumentSavingArgs class. An argument passed into [IDocumentSavingCallback.notify()](../idocumentsavingcallback/notify/#documentsavingargs)"
type: docs
weight: 130
url: /python-net/aspose.words.saving/documentsavingargs/
---

## DocumentSavingArgs class

An argument passed into [IDocumentSavingCallback.notify()](../idocumentsavingcallback/notify/#documentsavingargs).
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [estimated_progress](./estimated_progress/) | Overall estimated percentage progress. |

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

### See Also

* module [aspose.words.saving](../)


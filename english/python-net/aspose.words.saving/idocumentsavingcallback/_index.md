---
title: IDocumentSavingCallback class
linktitle: IDocumentSavingCallback class
articleTitle: IDocumentSavingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.saving.IDocumentSavingCallback class. Implement this interface if you want to have your own custom method called during saving a document."
type: docs
weight: 320
url: /python-net/aspose.words.saving/idocumentsavingcallback/
---

## IDocumentSavingCallback class

Implement this interface if you want to have your own custom method called during saving a document.


### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#documentsavingargs) | This is called to notify of document saving progress. |

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

* module [aspose.words.saving](../)


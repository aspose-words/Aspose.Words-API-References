---
title: IDocumentSavingCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for Python
description: "IDocumentSavingCallback.notify method. This is called to notify of document saving progress."
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
| args | [DocumentSavingArgs](../../documentsavingargs/) | An argument of the event. |

### Remarks

The primary uses for this interface is to allow application code to obtain progress status and abort saving process.


An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.




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
* class [IDocumentSavingCallback](../)


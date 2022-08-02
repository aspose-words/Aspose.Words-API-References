---
title: FileCorruptedException class
second_title: Aspose.Words for Python via .NET API Reference
description: "Thrown during document load, when the document appears to be corrupted and impossible to load."
type: docs
weight: 380
url: /python-net/aspose.words/filecorruptedexception/
---

## FileCorruptedException class

Thrown during document load, when the document appears to be corrupted and impossible to load.


### Examples

Shows how to catch a FileCorruptedException.

```python
try:
    # If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
    # chances are that we will get an exception thrown when trying to load that document using Aspose.Words.
    doc = aw.Document(MY_DIR + "Corrupted document.docx")
except Exception as error:
    print(error)
```

### See Also

* module [aspose.words](../)


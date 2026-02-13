---
title: FileCorruptedException class
linktitle: FileCorruptedException class
articleTitle: FileCorruptedException class
second_title: Aspose.Words for Python
description: "aspose.words.FileCorruptedException class. Thrown during document load, when the document appears to be corrupted and impossible to load"
type: docs
weight: 410
url: /python-net/aspose.words/filecorruptedexception/
---

## FileCorruptedException class

Thrown during document load, when the document appears to be corrupted and impossible to load.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Examples

Shows how to catch a FileCorruptedException.

```python
try:
    # If we get an "Unreadable content" error message when trying to open a document using Microsoft Word,
    # chances are that we will get an exception thrown when trying to load that document using Aspose.Words.
    doc = aw.Document(MY_DIR + 'Corrupted document.docx')
except Exception as error:
    print(error)
```

### See Also

* module [aspose.words](../)


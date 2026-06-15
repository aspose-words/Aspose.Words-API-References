---
title: TxtLoadOptions constructor
linktitle: TxtLoadOptions constructor
articleTitle: TxtLoadOptions constructor
second_title: Aspose.Words for Python
description: "TxtLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /python-net/aspose.words.loading/txtloadoptions/__init__/
---

## TxtLoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

### Examples

Shows how to read and display hyperlinks.

```python
input_text = 'Some links in TXT:\n' + 'https://www.aspose.com/\n' + 'https://docs.aspose.com/words/net/\n'
with io.BytesIO() as stream:
    buf = input_text.encode('ascii')
    stream.write(buf)
    stream.seek(0)
    load_options = aw.loading.TxtLoadOptions()
    load_options.detect_hyperlinks = True
    # Load document with hyperlinks.
    doc = aw.Document(stream=stream, load_options=load_options)
    # Print hyperlinks text.
    for field in doc.range.fields:
        print(field.result)
    assert doc.range.fields[0].result.strip() == 'https://www.aspose.com/'
    assert doc.range.fields[1].result.strip() == 'https://docs.aspose.com/words/net/'
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)


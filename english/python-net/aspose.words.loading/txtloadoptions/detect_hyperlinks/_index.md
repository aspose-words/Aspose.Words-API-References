---
title: TxtLoadOptions.detect_hyperlinks property
linktitle: detect_hyperlinks property
articleTitle: detect_hyperlinks property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.detect_hyperlinks property. Specifies either to detect hyperlinks in text"
type: docs
weight: 30
url: /python-net/aspose.words.loading/txtloadoptions/detect_hyperlinks/
---

## TxtLoadOptions.detect_hyperlinks property

Specifies either to detect hyperlinks in text.
The default value is ``False``.



```python
@property
def detect_hyperlinks(self) -> bool:
    ...

@detect_hyperlinks.setter
def detect_hyperlinks(self, value: bool):
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


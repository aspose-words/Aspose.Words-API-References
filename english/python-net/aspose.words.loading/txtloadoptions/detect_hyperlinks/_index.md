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
input_text = b'Some links in TXT:\nhttps://www.aspose.com/\nhttps://docs.aspose.com/words/python-net/\n'
stream_ = io.BytesIO()
stream_.write(input_text)
stream_.flush()
options = aw.loading.TxtLoadOptions()
options.detect_hyperlinks = True
doc = aw.Document(stream_, options)
stream_.close()
for field in doc.range.fields:
    print(field.result)
self.assertEqual('https://www.aspose.com/', doc.range.fields[0].result.strip())
self.assertEqual('https://docs.aspose.com/words/python-net/', doc.range.fields[1].result.strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)


---
title: RtfLoadOptions constructor
linktitle: RtfLoadOptions constructor
articleTitle: RtfLoadOptions constructor
second_title: Aspose.Words for Python
description: "RtfLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /zh/python-net/aspose.words.loading/rtfloadoptions/__init__/
---

## RtfLoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

### Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```python
# 创建一个 "RtfLoadOptions" 对象，以修改加载 RTF 文档的方式。
load_options = aw.loading.RtfLoadOptions()
# 将 "RecognizeUtf8Text" 属性设置为 "false"，以假设文档使用 ISO 8859-1 字符集
# 并加载文档中的每个字符。
# 将 "RecognizeUtf8Text" 属性设置为 "true"，以解析文本中可能出现的任何可变长度字符。
load_options.recognize_utf8_text = recognize_utf_8_text
doc = aw.Document(file_name=MY_DIR + 'UTF-8 characters.rtf', load_options=load_options)
self.assertEqual('“John Doe´s list of currency symbols”™\r' + '€, ¢, £, ¥, ¤' if recognize_utf_8_text else 'â€œJohn DoeÂ´s list of currency symbolsâ€\x9dâ„¢\r' + 'â‚¬, Â¢, Â£, Â¥, Â¤', doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [RtfLoadOptions](../)


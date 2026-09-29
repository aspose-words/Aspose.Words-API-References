---
title: RtfLoadOptions constructor
linktitle: RtfLoadOptions constructor
articleTitle: RtfLoadOptions constructor
second_title: Aspose.Words for Python
description: "RtfLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /ru/python-net/aspose.words.loading/rtfloadoptions/__init__/
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
# Создайте объект "RtfLoadOptions", чтобы изменить способ загрузки RTF‑документа.
load_options = aw.loading.RtfLoadOptions()
# Установите свойство "RecognizeUtf8Text" в значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
# и загружает каждый символ в документе.
# Установите свойство "RecognizeUtf8Text" в значение "true", чтобы разбирать любые переменно‑длинные символы, которые могут встречаться в тексте.
load_options.recognize_utf8_text = recognize_utf_8_text
doc = aw.Document(file_name=MY_DIR + 'UTF-8 characters.rtf', load_options=load_options)
self.assertEqual('“John Doe´s list of currency symbols”™\r' + '€, ¢, £, ¥, ¤' if recognize_utf_8_text else 'â€œJohn DoeÂ´s list of currency symbolsâ€\x9dâ„¢\r' + 'â‚¬, Â¢, Â£, Â¥, Â¤', doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [RtfLoadOptions](../)


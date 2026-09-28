---
title: RtfLoadOptions constructor
linktitle: RtfLoadOptions constructor
articleTitle: RtfLoadOptions constructor
second_title: Aspose.Words for Python
description: "RtfLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /ar/python-net/aspose.words.loading/rtfloadoptions/__init__/
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
# أنشئ كائن "RtfLoadOptions" لتعديل طريقة تحميل مستند RTF.
load_options = aw.loading.RtfLoadOptions()
# قم بتعيين خاصية "RecognizeUtf8Text" إلى "false" لتفترض أن المستند يستخدم مجموعة الأحرف ISO 8859-1
# ويحمّل كل حرف في المستند.
# قم بتعيين خاصية "RecognizeUtf8Text" إلى "true" لتحليل أي أحرف ذات طول متغيّر قد تظهر في النص.
load_options.recognize_utf8_text = recognize_utf_8_text
doc = aw.Document(file_name=MY_DIR + 'UTF-8 characters.rtf', load_options=load_options)
self.assertEqual('“John Doe´s list of currency symbols”™\r' + '€, ¢, £, ¥, ¤' if recognize_utf_8_text else 'â€œJohn DoeÂ´s list of currency symbolsâ€\x9dâ„¢\r' + 'â‚¬, Â¢, Â£, Â¥, Â¤', doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [RtfLoadOptions](../)


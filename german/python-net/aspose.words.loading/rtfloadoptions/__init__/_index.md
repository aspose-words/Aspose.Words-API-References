---
title: RtfLoadOptions constructor
linktitle: RtfLoadOptions constructor
articleTitle: RtfLoadOptions constructor
second_title: Aspose.Words for Python
description: "RtfLoadOptions constructor. Initializes a new instance of this class with default values."
type: docs
weight: 10
url: /de/python-net/aspose.words.loading/rtfloadoptions/__init__/
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
# Erstellen Sie ein "RtfLoadOptions"‑Objekt, um zu ändern, wie wir ein RTF‑Dokument laden.
load_options = aw.loading.RtfLoadOptions()
# Setzen Sie die Eigenschaft "RecognizeUtf8Text" auf "false", um anzunehmen, dass das Dokument den Zeichensatz ISO 8859-1 verwendet
# und jedes Zeichen im Dokument lädt.
# Setzen Sie die Eigenschaft "RecognizeUtf8Text" auf "true", um beliebige variable Zeichenlängen im Text zu verarbeiten.
load_options.recognize_utf8_text = recognize_utf_8_text
doc = aw.Document(file_name=MY_DIR + 'UTF-8 characters.rtf', load_options=load_options)
self.assertEqual('“John Doe´s list of currency symbols”™\r' + '€, ¢, £, ¥, ¤' if recognize_utf_8_text else 'â€œJohn DoeÂ´s list of currency symbolsâ€\x9dâ„¢\r' + 'â‚¬, Â¢, Â£, Â¥, Â¤', doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [RtfLoadOptions](../)


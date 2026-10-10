---
title: RtfLoadOptions.recognize_utf8_text property
linktitle: recognize_utf8_text property
articleTitle: recognize_utf8_text property
second_title: Aspose.Words for Python
description: "RtfLoadOptions.recognize_utf8_text property. When set to ``True``,  will try to detect UTF8 characters,  they will be preserved during import."
type: docs
weight: 20
url: /de/python-net/aspose.words.loading/rtfloadoptions/recognize_utf8_text/
---

## RtfLoadOptions.recognize_utf8_text property

When set to ``True``,  will try to detect UTF8 characters, 
they will be preserved during import.





```python
@property
def recognize_utf8_text(self) -> bool:
    ...

@recognize_utf8_text.setter
def recognize_utf8_text(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




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


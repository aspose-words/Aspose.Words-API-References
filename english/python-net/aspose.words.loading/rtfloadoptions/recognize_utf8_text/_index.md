---
title: recognize_utf8_text property
second_title: Aspose.Words for Python via .NET API Reference
description: "When set to ``True``, Aspose.Charset.CharsetDetector will try to detect UTF8 characters,  they will be preserved during import."
type: docs
weight: 20
url: /python-net/aspose.words.loading/rtfloadoptions/recognize_utf8_text/
---

## RtfLoadOptions.recognize_utf8_text property

When set to ``True``, Aspose.Charset.CharsetDetector will try to detect UTF8 characters, 
they will be preserved during import.



Default value is``False``.



### Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```python
# Create an "RtfLoadOptions" object to modify how we load an RTF document.
load_options = aw.loading.RtfLoadOptions()

# Set the "recognize_utf8_text" property to "False" to assume that the document uses the ISO 8859-1 charset
# and loads every character in the document.
# Set the "recognize_utf8_text" property to "True" to parse any variable-length characters that may occur in the text.
load_options.recognize_utf8_text = recognize_utf8_text

doc = aw.Document(MY_DIR + "UTF-8 characters.rtf", load_options)

if recognize_utf8_text:
    self.assertEqual(
        "“John Doe´s list of currency symbols”™\r" + "€, ¢, £, ¥, ¤",
        doc.first_section.body.get_text().strip())
else:
    self.assertEqual(
        "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" + "â‚¬, Â¢, Â£, Â¥, Â¤",
        doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../../)
* class [RtfLoadOptions](../)


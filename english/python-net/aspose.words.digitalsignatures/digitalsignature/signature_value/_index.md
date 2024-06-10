---
title: DigitalSignature.signature_value property
linktitle: signature_value property
articleTitle: signature_value property
second_title: Aspose.Words for Python
description: "DigitalSignature.signature_value property. Gets an array of bytes representing a signature value."
type: docs
weight: 70
url: /python-net/aspose.words.digitalsignatures/digitalsignature/signature_value/
---

## DigitalSignature.signature_value property

Gets an array of bytes representing a signature value.


```python
@property
def signature_value(self) -> bytes:
    ...

```

### Examples

Shows how to get a digital signature value from a digitally signed document.

```python
doc = aw.Document(MY_DIR + 'Digitally signed.docx')
for digital_signature_val in doc.digital_signatures:
    signature_value = base64.b64encode(digital_signature_val.signature_value)
    self.assertEqual(b'K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbDMhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=', signature_value)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignature](../)


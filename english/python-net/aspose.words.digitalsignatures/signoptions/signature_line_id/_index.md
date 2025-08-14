---
title: SignOptions.signature_line_id property
linktitle: signature_line_id property
articleTitle: signature_line_id property
second_title: Aspose.Words for Python
description: "SignOptions.signature_line_id property. Signature line identifier"
type: docs
weight: 60
url: /python-net/aspose.words.digitalsignatures/signoptions/signature_line_id/
---

## SignOptions.signature_line_id property

Signature line identifier.
Default value is **Empty (all zeroes) Guid**.



```python
@property
def signature_line_id(self) -> uuid.UUID:
    ...

@signature_line_id.setter
def signature_line_id(self, value: uuid.UUID):
    ...

```

### Remarks

When set, it associates [SignatureLine](../../../aspose.words.drawing/signatureline/) with corresponding [DigitalSignature](../../digitalsignature/).



### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)


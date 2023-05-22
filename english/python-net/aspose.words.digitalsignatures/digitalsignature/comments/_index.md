---
title: DigitalSignature.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Python
description: "DigitalSignature.comments property. Gets the signing purpose comment."
type: docs
weight: 20
url: /python-net/aspose.words.digitalsignatures/digitalsignature/comments/
---

## DigitalSignature.comments property

Gets the signing purpose comment.


### Examples

Shows how to validate and display information about each signature in a document.

```python
doc = aw.Document(MY_DIR + "Digitally signed.docx")

for signature in doc.digital_signatures:
    print(f"\n{'Valid' if signature.is_valid else 'Invalid'} signature: ")
    print(f"\tReason:\t{signature.comments}")
    print(f"\tType:\t{signature.signature_type}")
    print(f"\tSign time:\t{signature.sign_time}")
    # System.Security.Cryptography.X509Certificates.X509Certificate2 is not supported. That is why the following information is not accesible.
    #print(f"\tSubject name:\t{signature.certificate_holder.certificate.subject_name}")
    #print(f"\tIssuer name:\t{signature.certificate_holder.certificate.issuer_name.name}")
    print()
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignature](../)


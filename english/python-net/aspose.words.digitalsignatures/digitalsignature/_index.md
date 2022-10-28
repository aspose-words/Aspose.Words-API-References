---
title: DigitalSignature class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a digital signature on a document and the result of its verification"
type: docs
weight: 20
url: /python-net/aspose.words.digitalsignatures/digitalsignature/
---

## DigitalSignature class

Represents a digital signature on a document and the result of its verification.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [certificate_holder](./certificate_holder/) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [comments](./comments/) | Gets the signing purpose comment. |
| [is_valid](./is_valid/) | Returns ``True`` if this digital signature is valid and the document has not been tampered with. |
| [issuer_name](./issuer_name/) | Returns the subject distinguished name of the certificate isuuer. |
| [sign_time](./sign_time/) | Gets the time the document was signed. |
| [signature_type](./signature_type/) | Gets the type of the digital signature. |
| [subject_name](./subject_name/) | Returns the subject distinguished name of the certificate that was used to sign the document. |

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

* module [aspose.words.digitalsignatures](../)


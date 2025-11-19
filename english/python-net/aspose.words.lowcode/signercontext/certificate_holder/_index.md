---
title: SignerContext.certificate_holder property
linktitle: certificate_holder property
articleTitle: certificate_holder property
second_title: Aspose.Words for Python
description: "SignerContext.certificate_holder property. CertificateHolder object with certificate that used to sign file."
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/signercontext/certificate_holder/
---

## SignerContext.certificate_holder property

CertificateHolder object with certificate that used to sign file.


```python
@property
def certificate_holder(self) -> aspose.words.digitalsignatures.CertificateHolder:
    ...

@certificate_holder.setter
def certificate_holder(self, value: aspose.words.digitalsignatures.CertificateHolder):
    ...

```

### Remarks

The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set.


### See Also

* module [aspose.words.lowcode](../../)
* class [SignerContext](../)


﻿---
title: LoadOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "LoadOptions.password property. Gets or sets the password for opening an encrypted document"
type: docs
weight: 110
url: /python-net/aspose.words.loading/loadoptions/password/
---

## LoadOptions.password property

Gets or sets the password for opening an encrypted document.
Can be ``None`` or empty string. Default is ``None``.



```python
@property
def password(self) -> str:
    ...

@password.setter
def password(self, value: str):
    ...

```

### Remarks

You need to know the password to open an encrypted document. If the document is not encrypted, set this to ``None`` or empty string.




### Examples

Shows how to sign encrypted document file.

```python
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Create a comment, date, and decryption password which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
# Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.DecryptionPassword.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)


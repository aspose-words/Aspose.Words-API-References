﻿---
title: SignOptions.decryption_password property
linktitle: decryption_password property
articleTitle: decryption_password property
second_title: Aspose.Words for Python
description: "SignOptions.decryption_password property. The password to decrypt source document"
type: docs
weight: 30
url: /python-net/aspose.words.digitalsignatures/signoptions/decryption_password/
---

## SignOptions.decryption_password property

The password to decrypt source document.
Default value is **empty string** ().



```python
@property
def decryption_password(self) -> str:
    ...

@decryption_password.setter
def decryption_password(self, value: str):
    ...

```

### Remarks

If OOXML document is encrypted, you should provide decryption password
to decrypt source document before it will be signed.
This is not required for documents in binary DOC format.


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

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)


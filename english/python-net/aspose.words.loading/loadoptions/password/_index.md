---
title: password property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the password for opening an encrypted document"
type: docs
weight: 100
url: /python-net/aspose.words.loading/loadoptions/password/
---

## LoadOptions.password property

Gets or sets the password for opening an encrypted document.
Can be ``None`` or empty string. Default is ``None``.


You need to know the password to open an encrypted document. If the document is not encrypted, set this to ``None`` or empty string.




### Examples

Shows how to sign encrypted document file.

```python
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

# Create a comment, date, and decryption password which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = "Comment"
sign_options.sign_time = datetime.now()
sign_options.decryption_password = "docPassword"

# Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
input_file_name = MY_DIR + "Encrypted.docx"
output_file_name = ARTIFACTS_DIR + "DigitalSignatureUtil.decryption_password.docx"

aw.digitalsignatures.DigitalSignatureUtil.sign(input_file_name, output_file_name, certificate_holder, sign_options)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)


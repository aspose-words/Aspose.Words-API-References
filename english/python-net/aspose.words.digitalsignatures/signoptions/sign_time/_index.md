---
title: sign_time property
second_title: Aspose.Words for Python via .NET API Reference
description: "The date of signing"
type: docs
weight: 50
url: /python-net/aspose.words.digitalsignatures/signoptions/sign_time/
---

## SignOptions.sign_time property

The date of signing.
Default value is **current time** (System.DateTime.Now).



### Examples

Shows how to digitally sign documents.

```python
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

# Create a comment and date which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = "My comment"
sign_options.sign_time = datetime.now()

# Take an unsigned document from the local file system via a file stream,
# then create a signed copy of it determined by the filename of the output file stream.
with open(MY_DIR + "Document.docx", "rb") as stream_in:
    with open(ARTIFACTS_DIR + "DigitalSignatureUtil.sign_document.docx", "wb") as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(stream_in, stream_out, certificate_holder, sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)


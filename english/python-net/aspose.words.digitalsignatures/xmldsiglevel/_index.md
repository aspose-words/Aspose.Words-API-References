---
title: XmlDsigLevel enumeration
linktitle: XmlDsigLevel enumeration
articleTitle: XmlDsigLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.XmlDsigLevel enumeration. Specifies the level of a digital signature based on XML-DSig standard."
type: docs
weight: 70
url: /python-net/aspose.words.digitalsignatures/xmldsiglevel/
---

## XmlDsigLevel enumeration

Specifies the level of a digital signature based on XML-DSig standard.


### Members

| Name | Description |
| --- | --- |
| XML_D_SIG | Specifies XML-DSig signature level. |
| X_AD_ES_EPES | Specifies XAdES-EPES signature level. |

### Examples

Shows how to sign document based on XML-DSig standard.

```python
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.xml_dsig_level = aw.digitalsignatures.XmlDsigLevel.X_AD_ES_EPES
input_file_name = MY_DIR + 'Document.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.XmlDsig.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../)


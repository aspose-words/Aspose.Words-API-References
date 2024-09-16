---
title: SignOptions.xml_dsig_level property
linktitle: xml_dsig_level property
articleTitle: xml_dsig_level property
second_title: Aspose.Words for Python
description: "SignOptions.xml_dsig_level property. Specifies the level of a digital signature based on XML-DSig standard"
type: docs
weight: 80
url: /python-net/aspose.words.digitalsignatures/signoptions/xml_dsig_level/
---

## SignOptions.xml_dsig_level property

Specifies the level of a digital signature based on XML-DSig standard.
The default value is [XmlDsigLevel.XML_D_SIG](../../xmldsiglevel/#XML_D_SIG).



```python
@property
def xml_dsig_level(self) -> aspose.words.digitalsignatures.XmlDsigLevel:
    ...

@xml_dsig_level.setter
def xml_dsig_level(self, value: aspose.words.digitalsignatures.XmlDsigLevel):
    ...

```

### Remarks

Different levels of XAdES signatures can be created starting from Office 2010.


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

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)


---
title: Aspose::Words::DigitalSignatures::SignOptions class
linktitle: SignOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions class. Allows to specify options for document signing. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Allows to specify options for document signing. To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class SignOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Comments](./get_comments/)() const | Specifies comments on the digital signature. Default value is **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | The password to decrypt source document. Default value is **empty string**. |
| [get_ProviderId](./get_providerid/)() const | Specifies the class ID of the signature provider. Default value is **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Signature line identifier. Default value is **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | The image that will be shown in associated [SignatureLine](../../aspose.words.drawing/signatureline/). Default value is **null**. |
| [get_SignTime](./get_signtime/)() const | The date of signing. Default value is **current time** (**Now**). |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Comments](./set_comments/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_SignatureLineId](./get_signaturelineid/). |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_SignatureLineImage](./get_signaturelineimage/). |
| [set_SignTime](./set_signtime/)(System::DateTime) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) |  |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

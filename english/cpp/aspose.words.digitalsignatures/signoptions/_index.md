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
| [get_SignTime](./get_signtime/)() const | The date of signing. Default value is **current time** (**Now**) |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Specifies the level of a digital signature based on XML-DSig standard. The default value is [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Comments](./set_comments/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Signature line identifier. Default value is **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | The image that will be shown in associated [SignatureLine](../../aspose.words.drawing/signatureline/). Default value is **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Setter for [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Examples



Shows how to digitally sign documents. 
```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Create a comment and date which will be applied with our new digital signature.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

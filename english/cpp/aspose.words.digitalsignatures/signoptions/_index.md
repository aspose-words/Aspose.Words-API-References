---
title: Aspose::Words::DigitalSignatures::SignOptions class
linktitle: SignOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions class. Allows to specify options for document signing. To learn more, visit the Work with Digital Signatures documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Allows to specify options for document signing. 
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class SignOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |
| [get_ApplicationVersion](./get_applicationversion/)() const | Gets or sets the application version for the digital signature. Default value is "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Gets or sets the color depth for the digital signature. Default value is 32. |
| [get_Comments](./get_comments/)() const | Specifies comments on the digital signature. Default value is empty string. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | The password to decrypt source document. Default value is empty string. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Gets or sets the horizontal resolution for the digital signature. Default value is 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Gets or sets the Office version for the digital signature. Default value is "12.0". |
| [get_ProviderId](./get_providerid/)() const | Specifies the class ID of the signature provider. Default value is Empty (all zeroes) Guid. |
| [get_SignTime](./get_signtime/)() const | The date of signing. Default value is current time (**Now**) |
| [get_SignatureLineId](./get_signaturelineid/)() const | Signature line identifier. Default value is Empty (all zeroes) Guid. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | The image that will be shown in associated [SignatureLine](../../aspose.words.drawing/signatureline/). Default value is **null**. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA). The default value is **null** and the digital signature will not be time-stamped. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Gets or sets the vertical resolution for the digital signature. Default value is 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Gets or sets the Windows version for the digital signature. Default value is "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Specifies the level of a digital signature based on the XML-DSig standard. The default value is [XmlDSig](../xmldsiglevel/). |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String \&) | Sets the application version for the digital signature. Default value is "12.0". |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Sets the color depth for the digital signature. Default value is 32. |
| [set_Comments](./set_comments/)(const System::String \&) | Specifies comments on the digital signature. Default value is empty string. |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String \&) | The password to decrypt source document. Default value is empty string. |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Sets the horizontal resolution for the digital signature. Default value is 1920. |
| [set_OfficeVersion](./set_officeversion/)(const System::String \&) | Sets the Office version for the digital signature. Default value is "12.0". |
| [set_ProviderId](./set_providerid/)(System::Guid) | Specifies the class ID of the signature provider. Default value is Empty (all zeroes) Guid. |
| [set_SignTime](./set_signtime/)(System::DateTime) | The date of signing. Default value is current time (**Now**) |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Signature line identifier. Default value is Empty (all zeroes) Guid. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\> \&) | The image that will be shown in associated [SignatureLine](../../aspose.words.drawing/signatureline/). Default value is **null**. |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings\> \&) | Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA). The default value is **null** and the digital signature will not be time-stamped. |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Sets the vertical resolution for the digital signature. Default value is 1200. |
| [set_WindowsVersion](./set_windowsversion/)(const System::String \&) | Sets the Windows version for the digital signature. Default value is "6.1". |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Specifies the level of a digital signature based on the XML-DSig standard. The default value is [XmlDSig](../xmldsiglevel/). |
## Examples


Shows how to digitally sign documents.

```cpp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

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
        DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```
## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

---
title: "Aspose::Words::DigitalSignatures::SignOptions class"
linktitle: "SignOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DigitalSignatures::SignOptions class. Tillåter att specificera alternativ för dokumentsignering. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Tillåter att ange alternativ för dokumentsignering. För att lära dig mer, besök artikeln [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class SignOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Hämtar eller anger applikationsversionen för den digitala signaturen. Standardvärdet är "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Hämtar eller anger färgdjupet för den digitala signaturen. Standardvärdet är 32. |
| [get_Comments](./get_comments/)() const | Anger kommentarer på den digitala signaturen. Standardvärdet är **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | Lösenordet för att dekryptera källdokumentet. Standardvärdet är **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Hämtar eller anger den horisontella upplösningen för den digitala signaturen. Standardvärdet är 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Hämtar eller anger Office‑versionen för den digitala signaturen. Standardvärdet är "12.0". |
| [get_ProviderId](./get_providerid/)() const | Anger klass‑ID för signaturleverantören. Standardvärdet är **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Identifierare för signaturlinje. Standardvärdet är **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | Bilden som kommer att visas i associerad [SignatureLine](../../aspose.words.drawing/signatureline/). Standardvärdet är **null**. |
| [get_SignTime](./get_signtime/)() const | Datumet för signering. Standardvärdet är **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Hämtar eller anger den vertikala upplösningen för den digitala signaturen. Standardvärdet är 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Hämtar eller anger Windows‑versionen för den digitala signaturen. Standardvärdet är "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Anger nivån för en digital signatur baserad på XML-DSig‑standarden. Standardvärdet är [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Identifierare för signaturlinje. Standardvärdet är **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | Bilden som kommer att visas i associerad [SignatureLine](../../aspose.words.drawing/signatureline/). Standardvärdet är **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Sättare för [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man digitalt signerar dokument.
```cpp
// Skapa ett X.509‑certifikat från en PKCS#12‑butik, som bör innehålla en privat nyckel.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
// sedan skapa en signerad kopia av den bestämd av filnamnet på utdatafilströmmen.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Se även

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

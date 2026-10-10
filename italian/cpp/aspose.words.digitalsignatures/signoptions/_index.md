---
title: "Aspose::Words::DigitalSignatures::SignOptions classe"
linktitle: "SignOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DigitalSignatures::SignOptions classe. Consente di specificare le opzioni per la firma del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Consente di specificare le opzioni per la firma dei documenti. Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Ottiene o imposta la versione dell'applicazione per la firma digitale. Il valore predefinito è "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Ottiene o imposta la profondità di colore per la firma digitale. Il valore predefinito è 32. |
| [get_Comments](./get_comments/)() const | Specifica i commenti sulla firma digitale. Il valore predefinito è **stringa vuota**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | La password per decrittare il documento di origine. Il valore predefinito è **stringa vuota**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Ottiene o imposta la risoluzione orizzontale per la firma digitale. Il valore predefinito è 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Ottiene o imposta la versione di Office per la firma digitale. Il valore predefinito è "12.0". |
| [get_ProviderId](./get_providerid/)() const | Specifica l'ID classe del provider di firma. Il valore predefinito è **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Identificatore della linea di firma. Il valore predefinito è **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | L'immagine che verrà mostrata nella [SignatureLine](../../aspose.words.drawing/signatureline/) associata. Il valore predefinito è **null**. |
| [get_SignTime](./get_signtime/)() const | La data della firma. Il valore predefinito è **tempo corrente** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Ottiene o imposta la risoluzione verticale per la firma digitale. Il valore predefinito è 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Ottiene o imposta la versione di Windows per la firma digitale. Il valore predefinito è "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Specifica il livello di una firma digitale basato sullo standard XML-DSig. Il valore predefinito è [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Identificatore della linea di firma. Il valore predefinito è **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | L'immagine che verrà mostrata nella [SignatureLine](../../aspose.words.drawing/signatureline/) associata. Il valore predefinito è **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Setter per [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come firmare digitalmente i documenti.
```cpp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Crea un commento e una data che saranno applicati con la nostra nuova firma digitale.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Vedi anche

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

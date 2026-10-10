---
title: "Aspose::Words::DigitalSignatures::SignOptions Klasse"
linktitle: "SignOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::SignOptions Klasse. Ermöglicht das Festlegen von Optionen für die Dokumentenunterzeichnung. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Ermöglicht das Festlegen von Optionen für das Signieren von Dokumenten. Weitere Informationen finden Sie im [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) Dokumentationsartikel.

```cpp
class SignOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Liest oder setzt die Anwendungs-Version für die digitale Signatur. Standardwert ist "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Liest oder setzt die Farbtiefe für die digitale Signatur. Standardwert ist 32. |
| [get_Comments](./get_comments/)() const | Gibt Kommentare zur digitalen Signatur an. Standardwert ist **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | Das Passwort zum Entschlüsseln des Quelldokuments. Standardwert ist **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Liest oder setzt die horizontale Auflösung für die digitale Signatur. Standardwert ist 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Liest oder setzt die Office-Version für die digitale Signatur. Standardwert ist "12.0". |
| [get_ProviderId](./get_providerid/)() const | Gibt die Klassen-ID des Signaturanbieters an. Standardwert ist **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Kennung der Signaturzeile. Standardwert ist **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | Das Bild, das in der zugehörigen [SignatureLine](../../aspose.words.drawing/signatureline/) angezeigt wird. Standardwert ist **null**. |
| [get_SignTime](./get_signtime/)() const | Das Datum der Unterzeichnung. Standardwert ist **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Liest oder setzt die vertikale Auflösung für die digitale Signatur. Standardwert ist 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Liest oder setzt die Windows-Version für die digitale Signatur. Standardwert ist "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard an. Der Standardwert ist [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Kennung der Signaturzeile. Standardwert ist **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | Das Bild, das in der zugehörigen [SignatureLine](../../aspose.words.drawing/signatureline/) angezeigt wird. Standardwert ist **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Setter für [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man Dokumente digital signiert.
```cpp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, der einen privaten Schlüssel enthalten sollte.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Nehmen Sie ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
// und erstellen Sie dann eine signierte Kopie davon, bestimmt durch den Dateinamen des Ausgabedateistreams.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Siehe auch

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

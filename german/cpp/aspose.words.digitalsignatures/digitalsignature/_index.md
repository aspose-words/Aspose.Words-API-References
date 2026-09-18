---
title: "Aspose::Words::DigitalSignatures::DigitalSignature Klasse"
linktitle: "DigitalSignature"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::DigitalSignature Klasse. Stellt eine digitale Signatur in einem Dokument und das Ergebnis ihrer Verifizierung dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Stellt eine digitale Signatur in einem Dokument und das Ergebnis ihrer Verifizierung dar. Weitere Informationen finden Sie im [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) Dokumentationsartikel.

```cpp
class DigitalSignature : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Ermittelt die Anwendungsversion für die digitale Signatur. |
| [get_CertificateHolder](./get_certificateholder/)() const | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [get_ColorDepth](./get_colordepth/)() | Ermittelt die Farbtiefe für die digitale Signatur. |
| [get_Comments](./get_comments/)() | Ermittelt den Kommentar zum Signaturzweck. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Ermittelt die horizontale Auflösung für die digitale Signatur. |
| [get_IssuerName](./get_issuername/)() | Gibt den Distinguished Name des Zertifikatsausstellers zurück. |
| [get_IsValid](./get_isvalid/)() const | Gibt **true** zurück, wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde. |
| [get_OfficeVersion](./get_officeversion/)() | Ermittelt die Office-Version für die digitale Signatur. |
| [get_SignatureType](./get_signaturetype/)() const | Ermittelt den Typ der digitalen Signatur. |
| [get_SignatureValue](./get_signaturevalue/)() const | Ermittelt ein Byte-Array, das einen Signaturwert darstellt. |
| [get_SignTime](./get_signtime/)() const | Ermittelt die Zeit, zu der das Dokument signiert wurde. |
| [get_SubjectName](./get_subjectname/)() | Gibt den Distinguished Name des Subjekts des Zertifikats zurück, das zum Signieren des Dokuments verwendet wurde. |
| [get_VerticalResolution](./get_verticalresolution/)() | Ermittelt die vertikale Auflösung für die digitale Signatur. |
| [get_WindowsVersion](./get_windowsversion/)() | Ermittelt die Windows-Version für die digitale Signatur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Gibt eine benutzerfreundliche Zeichenkette zurück, die den Wert dieses Objekts anzeigt. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man jede Signatur in einem Dokument validiert und Informationen darüber anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```

## Siehe auch

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)

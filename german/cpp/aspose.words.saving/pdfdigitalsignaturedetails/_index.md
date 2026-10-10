---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails Klasse"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails Klasse. Enthält Details zum Signieren eines PDF-Dokuments mit einer digitalen Signatur in C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Enthält Details zum Signieren eines PDF‑Dokuments mit einer digitalen Signatur.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Liefert den Hash-Algorithmus. |
| [get_Location](./get_location/)() const | Liefert den Ort der Signatur. |
| [get_Reason](./get_reason/)() const | Liefert den Grund der Signatur. |
| [get_SignatureDate](./get_signaturedate/)() const | Liefert oder setzt das Datum der Signatur. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Liefert oder setzt die Einstellungen für den Zeitstempel der digitalen Signatur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Initialisiert eine Instanz dieser Klasse. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Initialisiert eine Instanz dieser Klasse. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Setzt den Hash-Algorithmus. |
| [set_Location](./set_location/)(const System::String\&) | Setzt den Ort der Signatur. |
| [set_Reason](./set_reason/)(const System::String\&) | Setzt den Grund der Signatur. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Setter für [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Setter für [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Hinweise


Derzeit ist das digitale Signieren von PDF-Dokumenten nur unter .NET 3.5 oder höher verfügbar.

Um ein PDF-Dokument digital zu signieren, wenn es von Aspose.Words erstellt wird, setzen Sie die Eigenschaft [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) auf ein gültiges [PdfDigitalSignatureDetails](./)-Objekt und speichern das Dokument anschließend im PDF-Format, indem Sie die [PdfSaveOptions](../pdfsaveoptions/) als Parameter an die Methode [Save()](../) übergeben.

Aspose.Words erstellt eine PKCS#7-Signatur über das gesamte PDF-Dokument und verwendet beim Erstellen einer digitalen Signatur den Filter "Adobe.PPKMS" sowie den Subfilter "adbe.pkcs7.sha1".

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)

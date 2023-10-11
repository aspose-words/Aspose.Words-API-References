---
title: Class PdfDigitalSignatureDetails
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfDigitalSignatureDetails klas. Enthält Details zum Signieren eines PDFDokuments mit einer digitalen Signatur.
type: docs
weight: 5430
url: /de/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Enthält Details zum Signieren eines PDF-Dokuments mit einer digitalen Signatur.

```csharp
public class PdfDigitalSignatureDetails
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Initialisiert eine Instanz dieser Klasse. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Gibt das Zertifikatsinhaberobjekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Ruft den Hash-Algorithmus ab oder legt ihn fest. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Ruft den Ort der Signatur ab oder legt diesen fest. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Ruft den Grund für die Signatur ab oder legt diesen fest. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Ruft das Datum der Unterzeichnung ab oder setzt es. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Ruft die Zeitstempeleinstellungen für die digitale Signatur ab oder legt diese fest. |

### Bemerkungen

Derzeit ist das digitale Signieren von PDF-Dokumenten nur für .NET 2.0 oder höher verfügbar.

Um ein PDF-Dokument bei der Erstellung durch Aspose.Words digital zu signieren, legen Sie fest[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) -Eigenschaft zu einer gültigen`PdfDigitalSignatureDetails` Objekt und speichern Sie dann das Dokument im PDF-Format unter Übergabe von [`PdfSaveOptions`](../pdfsaveoptions/) als Parameter in die[`Save`](../../aspose.words/document/save/) Methode.

Aspose.Words erstellt eine PKCS#7-Signatur für das gesamte PDF-Dokument und verwendet beim Erstellen einer digitalen Signatur den Filter „Adobe.PPKMS“ und den Unterfilter „adbe.pkcs7.sha1“.

### Beispiele

Zeigt, wie ein generiertes PDF-Dokument signiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Konfigurieren Sie das „DigitalSignatureDetails“-Objekt des „SaveOptions“-Objekts für
// Signieren Sie das Dokument digital, während wir es mit der Methode „Speichern“ rendern.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)



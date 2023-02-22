---
title: Class PdfDigitalSignatureDetails
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfDigitalSignatureDetails klas. Enthält Details zum Signieren eines PDFDokuments mit einer digitalen Signatur.
type: docs
weight: 5150
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
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Ruft den Ort der Signatur ab oder legt ihn fest. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Ruft den Grund für die Signatur ab oder legt ihn fest. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Ruft das Datum der Unterzeichnung ab oder setzt es. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Ruft die Zeitstempeleinstellungen der digitalen Signatur ab oder legt sie fest. |

### Bemerkungen

Momentan ist das digitale Signieren von PDF-Dokumenten nur auf .NET 2.0 oder höher verfügbar.

Um ein PDF-Dokument digital zu signieren, wenn es von Aspose.Words erstellt wird, legen Sie die[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) -Eigenschaft in eine gültige`PdfDigitalSignatureDetails` Objekt und speichern Sie dann das Dokument im PDF-Format, indem Sie übergeben[`PdfSaveOptions`](../pdfsaveoptions/)als Parameter in die[`Save`](../../aspose.words/document/save/) Methode.

Aspose.Words erstellt eine PKCS#7-Signatur über das gesamte PDF-Dokument und verwendet beim Erstellen einer digitalen Signatur den „Adobe.PPKMS“-Filter und den „adbe.pkcs7.sha1“-Subfilter.

### Beispiele

Zeigt, wie ein generiertes PDF-Dokument signiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Konfigurieren Sie das "DigitalSignatureDetails"-Objekt des "SaveOptions"-Objekts zu
// das Dokument digital signieren, während wir es mit der "Save"-Methode rendern.
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)



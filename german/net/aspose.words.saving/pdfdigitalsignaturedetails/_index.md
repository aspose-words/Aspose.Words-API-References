---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.PdfDigitalSignatureDetails für nahtloses digitales Signieren von PDF-Dateien. Verbessern Sie die Dokumentensicherheit durch einfache Integration und robuste Funktionen.
type: docs
weight: 6220
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
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Gibt das Zertifikatsinhaberobjekt zurück, das das zum Signieren des Dokuments verwendete Zertifikat enthält. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Ruft den Hash-Algorithmus ab oder legt ihn fest. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Ruft den Speicherort der Signatur ab oder legt ihn fest. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Ruft den Grund für die Signatur ab oder legt ihn fest. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Ruft das Datum der Unterzeichnung ab oder legt es fest. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Ruft die Zeitstempeleinstellungen für die digitale Signatur ab oder legt sie fest. |

## Bemerkungen

Derzeit ist das digitale Signieren von PDF-Dokumenten nur unter .NET 3.5 oder höher verfügbar.

Um ein PDF-Dokument digital zu signieren, wenn es von Aspose.Words erstellt wird, setzen Sie die[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) -Eigenschaft auf einen gültigen`PdfDigitalSignatureDetails` Objekt und speichern Sie das Dokument dann im PDF-Format mit der Angabe [`PdfSaveOptions`](../pdfsaveoptions/) als Parameter in die[`Save`](../../aspose.words/document/save/) Verfahren.

Aspose.Words erstellt eine PKCS#7-Signatur über das gesamte PDF-Dokument und verwendet beim Erstellen einer digitalen Signatur den Filter „Adobe.PPKMS“ und den Unterfilter „adbe.pkcs7.sha1“.

## Beispiele

Zeigt, wie ein generiertes PDF-Dokument signiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Konfigurieren Sie das Objekt "DigitalSignatureDetails" des Objekts "SaveOptions" auf
// Signieren Sie das Dokument digital, während wir es mit der Methode „Speichern“ rendern.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)

---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words PdfDigitalSignatureHashAlgorithm, die digitale Hash-Algorithmen für sichere digitale Signaturen in Ihren Dokumenten definiert.
type: docs
weight: 6230
url: /de/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Gibt einen digitalen Hash-Algorithmus an, der von einer digitalen Signatur verwendet wird.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Sha256 | `0` | SHA-256-Hash-Algorithmus. |
| Sha384 | `1` | SHA-384-Hash-Algorithmus. |
| Sha512 | `2` | SHA-512-Hash-Algorithmus. |
| RipeMD160 | `3` | RIPEMD-160-Hash-Algorithmus. |

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

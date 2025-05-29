---
title: PdfDigitalSignatureDetails.SignatureDate
linktitle: SignatureDate
articleTitle: SignatureDate
second_title: Aspose.Words für .NET
description: Entdecken Sie die SignatureDate-Eigenschaft von PdfDigitalSignatureDetails, um Signaturdaten für Ihre Dokumente einfach zu verwalten und anzupassen. Optimieren Sie noch heute Ihren digitalen Workflow!
type: docs
weight: 60
url: /de/net/aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/
---
## PdfDigitalSignatureDetails.SignatureDate property

Ruft das Datum der Unterzeichnung ab oder legt es fest.

```csharp
public DateTime SignatureDate { get; set; }
```

## Bemerkungen

Der Standardwert ist die aktuelle Uhrzeit.

Dieser Wert erscheint in der digitalen Signatur als ungeprüfte Computerzeit.

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

* class [PdfDigitalSignatureDetails](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

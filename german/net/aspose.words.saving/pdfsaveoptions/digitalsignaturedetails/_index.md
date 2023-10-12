---
title: PdfSaveOptions.DigitalSignatureDetails
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Ruft die Details zum Signieren des ausgegebenen PDFDokuments ab oder legt diese fest.
type: docs
weight: 70
url: /de/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Ruft die Details zum Signieren des ausgegebenen PDF-Dokuments ab oder legt diese fest.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

### Bemerkungen

Der Standardwert ist`Null`und das Ausgabedokument wird nicht signiert. Wenn diese Eigenschaft auf einen gültigen Wert gesetzt ist[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, dann wird das ausgegebene PDF-Dokument digital signiert.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


